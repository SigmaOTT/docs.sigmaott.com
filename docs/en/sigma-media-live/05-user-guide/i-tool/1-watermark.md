---
title: Check watermark
order: 4
---

# Check watermark

The Watermark Check function of the Sigma Media-live service is designed to support detection, detection and inspection of audio files embedded watermarked into the original audio signal, for the purpose of protecting ownership and detecting unauthorized reproductions.

Scope: Profiles for all components of the Sigma Media-live service.

There are two methods to perform a watermark check.

## Check watermark with file

### Prepare the file

Before you start, you need to prepare a valid audio file.

- We support many audio file formats, including:

  - MP3 (MPEG Audio Layer III)

  - AAC (Advanced Audio Coding)

  - WAV (Waveform Audio File Format)

  - AIFF (Audio Interchange File Format)

  - FLAC (Free Lossless Audio Codec)

  - OGG (Ogg Vorbis)

  - M4A (MPEG-4 Audio)

  - AMR (Adaptive Multi-Rate)

  - WMA (Windows Media Audio)

  - APE (Monkey's Audio)

- Supported codecs: aac, mp3, pcm\*, mp2, opus

- A valid audio file size is less than 50 MB.

### Start testing

**Step 1**: Click Watermarking in the TOOL header menu.

A Check Watermarking pop-up window will appear.

! [Check watermarking] (/images/media-live/watermark/upload.png)

By default, display the 'Upload' option.

Users can perform the following actions:

- Drag and drop files
- Select the file from a personal computer.

**Step 2**:
The user uploads the file.

After selecting the file, the results displayed include:

- Selected filename
- The 'X' icon allows deleting files.

The user clicks the test button.

**Step 3**: Show the test process.

**The system performs the watermarking test at intervals of 20 seconds.** Users can cancel the watermarking check by clicking the 'Cancel' button, which returns to the upload interface.

## Check watermark with live recording

If you want to make the process quick, use the recording feature.
Before you begin, make sure the audio watermark test content is recorded from the stream to be tested through an electronic device, provided that the ambient noise level is maintained at a minimum to improve accuracy.

Give permission to use the microphone for the tool, connect your device to the device with the microphone integration.

### Start testing

**Step 1**: User selects Record in the pop-up Check watermarking window. Display the corresponding recording request information in the watermarking Test pop-up window.

! [Check watermarking] (/images/media-live/watermark/record.png)

**Step 2**: Click the recording icon. Connect the device successfully.

- Make a recording.

- Disable the 'check' button.

**Step 3**: Click the stop icon.

_In case the user does not stop, the system will automatically stop when the 20-second limit is reached._

- Show records

- The back icon and other **Check recordings** allow the user to make a recording.

- Turn on the 'test' button.

_In case the user clicks the **Check other records** icon the system will perform the recording again according to step 2._

**Step 4**: Click the 'Check' button.

**The system performs the testing process during the live recording period**.

! [Check watermarking] (/images/media-live/watermark/check.png)

Users can cancel the watermarking check by clicking the 'Cancel' button, which returns to the upload interface.

## Test results

After checking within the specified time period, the result will be displayed as follows:

! [Check watermarking] (/images/media-live/watermark/result.png)

1. If **watermark not found**: Message **No watermark found.**
2. Find watermark

- Show the ID of the watermarking and offer the option to copy.

- If **1 channel is found**: Displays the details of that channel, the icon points directly to the corresponding channel details, all on the same tab.

- If **multiple channels**: Display **total channels**, display scrollbar, icon pointing directly to corresponding channel details, all on the same tab.

- If \*\*no channel found: Displays string, which can be copied for use.

## The test failed

### Invalid upload

Only allow uploads of files that meet the regulations listed earlier. When the user clicks the test button, the system conducts a check, detects an unsupported file and displays a message in the right corner of the screen:

**Invalid file, please select another file.**

### No speakerphone access

Access to equipment is a prerequisite during the recording test. When the user clicks the recording icon and the process cannot continue, the system displays a message like this:

- Subject: Please grant permission to use the microphone for the tool.
- Contents: Check your system settings to make sure Sigma streaming has access to your microphone and try again.

### Exceeding system test time

During the inspection, something went wrong. After a test time of more than 20 seconds without results, the system displays the message:

**Process error, please try again.**
