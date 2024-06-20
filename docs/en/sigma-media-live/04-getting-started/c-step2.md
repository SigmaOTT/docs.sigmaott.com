---
title: "Step 2: Create new input"
order: 4
---

# Step 2: Create new input

You must create an input. The input identifies the media data stream that the Sigma Transcode Live system uses for transcoding or packaging.

The Sigma Streaming Platform system supports the following input standards:

- MPEG-TS over multicast UDP
- RTMP push
- RTMP pull
- RTP
- RTCP
- SRT push
- SRT pull

**Example of creating 1 multi cast UDP input**

1. Log in to the Sigma Streaming portal and open Transcode Live

2. Click the Add\*\*\* button in the **Input** menu in the Transcode\*\* section. The Input initialization interface will appear

3. Enter the required information
   1. **Name** of input
   2. **Redundancy** select **single**
   3. **Type** select **UDP**
   4. **Primary Source** fill in the prepared flow information in step 1 [Input Flow Settings](./b-step1.md)
   5. **Primary Interface Network** Please select 1 network card that receives this multicast UDP stream bypassing

! [Create Input] (/images/media-live/um-create-input.png)

_Note: If you do not fill in the information about the network card, the system will automatically get it from the default network card of the machine_

### Input configuration details

Please visit:

1. [Input configuration for Transcode channel] (.. /05-resource-input/01-transcode-input.md)
2. [Input Configuration for Package Channel] (.. /05-resource-input/02-package-input.md)
