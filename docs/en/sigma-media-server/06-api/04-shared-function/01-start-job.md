---
title: Job Initialization
order: 1
---

# Job Initialization

The Initialize Job function is used for both cases: creating a new channel and updating a running channel.

- If **name** matches an existing Job, the Job will be updated.
- If **name** does not match the existing Job, the Job will be created.

::: info

- Job's configuration parameters will not be saved when the server is turned off.
- Use the **mode** field to create a job for Live Channel or VOD Content.
- The **name** field is a unique identifier for the job and is used to update or disable the job.
  :::

## Request

sample

```json
{
  "type": "start",
  "name": "VTV3",
  "mode": "live",
  "gpu": -1,
  "input": {
    "main": "udp://234.5.6.7:8888",
    "backup": "udp://234.5.6.7:7777"
  },
  "target": [
    {
      "enable": 0,
      "format": "rtmp",
      "URL": "rtmp://localhost/app/stream",
      "select": [
        "128k",
        "360"
      ]
    },
    {
      "enable": 1,
      "format": "hls",
      "url": "/mnt/ramdisk/origin04/source/",
      "select": [
        "128k",
        "360"
      ]
    },
    {
      "enable": 0,
      "format": "dash",
      "url": "/mnt/ramdisk/origin04/360/",
      "select": [
        "128k",
        "360",
        "source"
      ],
      "manifest":{
      },
      "DRM:{
      }
    }
  ],
  "profile": [
    {
      "enable": 0,
      "id": "data",
      "type": "data",
      "codec": "copy",
      "streamIndex": 0,
      "sourceIndex": 0,
      "iframe": 50
    },
    {
      "ID": "96K",
      "type": "audio",
      "codec": "aac",
      "bitrate": 96000
    },
    {
      "id": "360",
      "type": "video",
      "codec": "h264",
      "width": 640,
      "height": 360,
      "bitrate": 500000,
      "CBR": 1,
      "pixelFormat": "yuv420p",
      "watermark": [
        {
          "enable": 1,
          "x": 10,
          "Y": 20,
          "URL": "wm.png"
        }
      ]
    },
    {
      "id": "source",
      "type": "video",
      "Codec": "copy"
    }
  ],
  "option": {
    "syncCopy": 1,
    "blackout": {
      "input": "blackout.jpg"
    }
  },
  "watermark":
  {
    "enable": 1,
    "x": 10,
    "Y": 20,
    "URL": "wm.png"
  },
  "thumb": {
    "enable": 1,
    "width": 300,
    "delay": 6,
    "name":"%d.jpg",
    "URL": "/mnt/ramdisk/origin05/trial/thumb/"
  }
}
```

Where:

- **Struct**: basic structure
  - **name**: channel identifier to toggle on and off
  - **GPU**: GPU chip order, GPU list taken at dump command (NVIDIA only supported), -1 is CPU usage
  - **input**: input list
  - **profile**: list of profiles
  - **target**: target list
  - **watermark**: Common watermark for channel, if multiple array is used
  - **thumb**: create thumnail for the channel, if many use array
  - **option**: additional settings
  - **input**: can be 1 string, string array (multiple inputs), or 1 object for the channel with backup

### Ingredients in detail

- **profile**
  - **id**: the identifier of the profile, if in the form of hex[0x10->0x1ffe] will be used as stream_id in the output video
  - **streamIndex**: the order of the original stream in the input, for example, the input has 2 audios, you can set the audio to 0, 1
  - **sourceIndex**: the order of input
  - **type**: [video, audio, data]
  - **Audio**:
    - **sampleRate**: [44100(default), 48000]
    - **channel**: [1, 2(default), 6(5.1)]
    - **codec**: [copy, aac(default), ac3, eac3, mp2]
    - **profile**(AAC only): [aac_low(default), aac_he, aac_he_v2, aac_main, aac_ld, aac_eld]
    - **volume**: change volume from original stream
      - "+5dB", "-10dB": change by 1 amount)
      - 0.5, 2 : 1 halving, double
      - "loudnorm": automatic according to EBU R128 standard
    - **language**: [2 characters string] en, vi, fr...
    - **group**: [string] group id
    - **label**: [string] display in player
  - **Video**:
    - **fps**: [20, 25(default), 30, 29.97, 59.94, 60]
    - **codec**: [H264(default), HEVC]
    - **pixelFormat**: [yuv420p(default), yuv444p, yuv420p10le, yuv444p10le]
    - **width, height**: [0, height], [width, 0], [width, height]
    - **bitrate, minrate, maxrate, bufsize**: config bitrate
    - **scaleType**: [fitWidth, fitHeight, fitInside, fitCrop, fitBoth, source]
      (note: if you leave width, height, scaleType in the total option, the source will scale before further processing)
    - **CBR**: [0, 1], Constant Bitrate mode enabled
    - **CQ**: [0 -> 51], Constant Quality mode
    - **VMAF**: [90 -> 92], target VMAF for Pte
    - **interlaced**: [0, 1], interlaced video mode
    - **watermark**: separate watermark for profile
    - **profile, level**: [baseline(for GPU), Main 3.0 | 4.0, High 4.0 | 4.1 | 4.2]
    - **Preset**:
      - CPU: [VeryFast, Superfast]
      - GPU: [LLHP, LLHQ]
    - **RC**(GPU only): [cbr_hq, cbr_hp] for CBR, [vbr_hq, vbr_hp] for VBR, Rate Control write for Preset
    - **iframe**: set iframe
      - -1: Automatic detection based on manifest.ts
      - 0 : according to the source
      - [1->16]: seconds
      - [17->300]: Number of frames
    - **hdr**(pixelFormat yuv420p10le recommended, hevc codec): [copy, none, hdr10, hlg10, pq10] supports HDR output, currently only supports MP4 containers (dash or hls+fmp4)
  - **data**: only copy codecs are supported

- **target**:
  - **format**: [RTMP, UDP, HLS, DASH, MSS, HDS, MP3, MP4, SRT, AAC, WAV, WEBVTT]
  - **select**: configure the output profile, each element can be profileId, profileId array, object
    - profileId: used for simple cases such as dash, mss
    - profileId array: used when you want to group audio, video for hls, hds, for example:
      select:[
      [
      "480p",
      "480p-audio"
      ]
      ]
    - object: used when you want to configure details for each profileId or profileId array, then the object will contain its own select and DRM object if any, for example:
      select:[
      {
      "title":"VTV3", // Channel title for udp
      "id": 15, // programId for udp
      "DRM":{
      "server":"http://drmproxy.com",
      "filter":"widevine+playready+fairplay"
      },
      "select": [
      "480p",
      "480p-audio"
      ]
      }
      ]
  - **DRM**: DRM configuration
    - Type:
      AES_128: HLS
      SAMPLE_AES: HLS TS(Fairplay)
      SAMPLE_AES_CTR, SAMPLE_AES_CBC: HLS FMP4, Dash
    - filter: [fairplay, widevine, playready, hls_widevine, hls_playready, dash_widevine, dash_playready], for multiDRM, filter DRM system for manifest
    - Direct use:
      - **URI**: Key URI for HLS
      - **key, keyId, iv**: base64
      - **widevine, playready**: base64 of PSSH respectively
      - **systems**: [{"id":"systemId(edef8ba979d64acea3c827dcd51d21ed for widevine", "uri": "skd://...", "pssh": "base64 of pssh data"}]
      - **expireTime**: the number of seconds that will retrieve the key information (used for proxy mode)
    - Use proxy: data returned as {data: {drm info khi dùng trực tiếp}}
      - **Server**: URL to get information
      - **body**: body for request to server
  - **Manifest**(for Dash, HLS)
    - **ts**: [2 -> 10], ts duration

    - **enableTime**(hls): [0, 1], insert timestamp into playlist

    - **appendList**(hls): [0, 1], serial to old playlist

    - **endList**(hls): [0, 1], insert endlist tag at end

    - **cache**: [-1 -> n] the number of files TS retains when deleted from the playlist, -1 is retained

    - **count**: [0 -> N], the number of TS kept in the playlist file, 0 is the whole

    - **singleFile**: [0, 1], enable non-split file mode

    - **fmp4**: [0, 1], use fmp4 format for segment

    - Manage names, paths:
      - Pattern support:
        - **%%d, %%06d**: index of TS
        - **%%b**: Bitrate of profile (only used for MSS, HDS)
        - **%v**: the name of the video profile (or audio if there is no video)
        - **%%r**: Add random numbers
        - **%%t**: add ts startPts, used only for tsName dash
        - \*\*., .. \*\*: relative path from primary URL
      - **masterName, masterPath, tsName, tsPrefix, initName, initPrefix, initPath**
      - **indexName, indexPath, indexPrefix**: only for dash
      - MSS only supports %%b, %%d
      - hds tsName is required to be Seg1-Frag%%d, at the same time tsPrefix must be non-empty (to avoid errors on some players), it is recommended to use: tsPrefix="%v/" tsPath "./%v/"

    - **persistent**: [0, 1], keep HTTP connection when writing files

    - **masterExtra**: [string array separated by commas], write down the master file with some other names

    - **chunked**: [0.01 -> n], the number of seconds of chunk when using lowlatency or mp4

    - **chunkedType**: ["fragment","range", "combine"], type low latency split or byte-range, default: fragment

    - **segment**: [0 -> n], the number of seconds of cutting the video when using mp4 format

    - **targetLatency**: [0 -> n], the number of latency seconds for lowlatency

    - **minLatency**: [0 -> n], the number of seconds min latency for lowlatency(dash)

    - **maxLatency**: [0 -> n], the number of seconds max latency for lowlatency(dash)

    - **header**: custom object for header

    - **buffer**: [0 -> 60], buffer time (suggestedPresentationDelay for dash, #EXT-X-START:TIME-OFFSET for hls)

    - **useThread**: [0, 1], open thread for sending manifest

- **watermark**: coordinates, wm size will base on 1920x1080 if there is no scale
  - **x, y**: [0 -> 1920, 0 -> 1080]coordinates on video
  - **id**: identifier to toggle on and off
  - **scale**: [0.1 -> 3.0], watermark size scale + coordinates if needed
  - **mediaScale**: [0.1 -> 3.0], content scale before processing
  - **delay**: [0 -> 120], the number of seconds that stop between 2 loops, used for dynamic watermarking
  - **enable**: [0, 1], hidden or visible, API controlled

- **Thumbnails**
  - **width**: [100 -> 1920]
  - **delay**: [1 -> 60], time between 2 images
  - **col, row**: [0 -> 10], used to create a tile for thumb, disabled by default

- **option**
  - **syncCopy**: [0 - > 2], default 0(disable), sync copy and transcode streams, 1 = drop non-idr keyframe, 2 = all frame
  - **timeout**: [2 -> 10], default 6, thread breaks if stopped at input, output, transcode
  - **syncStream**: [1 -> n], default 1, interrupt the stream if the sound and picture are offset
  - **GPU**: [-1, N], GPU override in config
  - **filterComplex**: custom filter for transcode (can use drag-and-drop interface on CMS to create)
  - **xerror**: [0, 1] Channel reset if a potentially faulty packet is detected
  - **maxSpeed**: [0.1 -> 10], (default 1.1), maximum channel speed
  - **loop**: [0, n], number of file loops
  - **limitInput**: [256 -> 2048], default 1024, maximum number of queue packets for slow processing
  - **copyts**: [0, 1], copy timestamp from original stream, default enabled for hash-only channel
  - **fixAac**: [0, 1], faulty AAC packet handling(causes player to stop on smartTV)
  - **sound**: audio file when running pre event using image
  - **preload**: [0, 1], renormalize video before running video pre events
  - **id3**: [0, 1], add stream id3 to HLS TS outputs
  - **s3Config**: the path to the s3 config file (s3 url is in the form s3://path/to/file), the default is data/s3.json, the file content is as follows:
  - ```json
    {
        "accessKeyId": "<required>",
        "secretAccessKey": "<required>",
        "Bucket": "<required>",
        "endpoint": "<optional>",
        "region": "<optional>"
    }
    ```

## Response

Success syntax

```json
{
  "ec": 0,
  "result": {
    "$job_name": "done"
  }
}
```
