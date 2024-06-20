---
title: Create a new profile
order: 1
---

# Profile

The profile profile information includes some important information for configuring the video conversion process. This information may vary depending on the specific platform, application, or tool the user is using to convert the video, to ensure that the generated video is of good quality and compatible with the viewer's device and network.

### Purpose

Support users to have the ability to choose and customize the profile as desired when creating channels.

### Scope

This profile is used for all features of the media-live service.

# Create a new profile

Create a new profile by following these steps:
**Step 1**: In the profile list, click the '+Add New' button in the right corner of the screen.
The system will display a pop-up **Add new profile**\* in the middle of the screen.

! [Create New] (/images/media-live/profile/create.png)

- Default display of profile name in the form: 'profile_[number due to random system]' helps users optimize time during the configuration process.
- Preset style selection

**Step 2**:

After clicking on the preset type, display a dropdownlist of 2 options:

- [Existing preset](./1-create-profile#existing-preset)
- [New preset](./1-create-profile#new-preset)

### Presets already exist

For quick configuration, users can select 'existing presets' – presets configured in the system.
The system will display a window.

! [Preset already exists] (/images/media-live/profile/existing-video.png)

The list of presets includes:

- Title: Add [video/audio/data] respectively
- The list includes:
  - ID
  - Name: the name of the preset
  - Type: [video/ audio/ data] respectively
  - Information: Profile details
  - Describe
- Pagination
- Refresh

**Step 3**: The user selects a preset from the list.

The system will return to the Create new profile pop-up window with updated data from the selected preset.

### New preset

To customize the media profile as desired, the user selects 'New Preset'. The system will display the corresponding media list information.

Names and descriptions are displayed by default in all preset types:

- Preset name: Block special characters, no spaces, support dashes, underscores. Vietnamese language is not supported.
- Preset description: Block special characters, **with spaces**, support dashes, underscores. Vietnamese language is not supported.

Details of each preset:

- [Video](./create-profile#video)
- [Audio](./create-profile#audio)
- [Data](./create-profile#data)

### Video

Only **1 video is allowed**.

The user selects the 'video' item, then displays the following information:

![video](/images/media-live/profile/create-data.png)

| School name          | Describe                                                                                                                                                                                     | Compulsory | Data type     | Default             | Rule                                                                                                         |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ------------- | ------------------- | ------------------------------------------------------------------------------------------------------------ |
| Kind                 | Preset type                                                                                                                                                                                  | Have       | Textbox       | **Video**           | Disable does not allow editing.                                                              |
| Codec                | Use to compress and decompress audio or video data to reduce size and increase transmission capacity.                                                                        | Have       | Single select | h264                | Options: h264, hevc, copy<br />**With copy option not allowed to edit other configurations** |
| Video rate           | Measure the data transfer speed of video or audio.                                                                                                                           | Not        | Integer       | 64000               | 64000 <= birate <= 60000000                                                                                  |
| FPS                  | The number of frames is displayed in one second.                                                                                                                             | Not        | Integer       | 10                  | 10 <= FPS <= 60                                                                                              |
| Width                | The width of the video frame, usually measured in pixels.                                                                                                                    | Not        | Integer       | 0                   | **0 <= Width <=7680**                                                                                        |
| Height               | The height of the video frame, usually measured in pixels.                                                                                                                   | Not        | Integer       | 0                   | **0 <= height<= 4320**                                                                                       |
| Hdr                  | High Dynamic Range is an image standard with multiple dynamic dynamic ranges, allowing the monitor to display clear images, especially details in floating and shadow areas. | Not        | Single select |                     | Options: Copy, none, HDR10, HLG10, PQ10                                                      |
| Bframe               | As a kind of frame in a video sequence, used to optimize video compression and quality.                                                                                      | Not        | Float         | 0.0 | 0.0 <= Bframe <= 3.0                                                         |
| Pixel format         | It is the way that each pixel in the image is represented and stored.                                                                                                        | Not        | Single select | Choose              | Options: yuv420p, yuv444p, yuv420p10le, yuv444p10le                                          |
| Scale Type           | Determine how the size ratio of the video, be it a fixed rate or an automatic change rate.                                                                                   | Not        | Single select | Choose              | Options: fitWidth, fitHeight, fitInside, fitCrop, fitBoth, source                            |
| Constant quality     | Make sure that the quality of the video does not change, despite fluctuations in content or deliverability.                                                                  | Not        | Integer       | 0                   | 0 <= constant quality <= 51                                                                                  |
| Interlaced mode      | A type of visual-in-video display in which odd and even lines are displayed alternately to create an image.                                                                  | Not        | Switch        | Disable             | Only used for input, not visible to viewers                                                                  |
| Constant birate mode | Keep the bitrate constant in case of a change in content or transmitting capacity.                                                                                           | Not        | Switch        | Disable             | Only used for input, not visible to viewers                                                                  |

### Audio

Allows maximum selection **10 audio**.

The user selects the 'audio' item, then displays the following information:

! [Audio] (/images/media-live/profile/audio.png)

| School name | Describe                                                                                                                                                                    | Compulsory | Data type | Default   | Rule                                                                                                                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Kind        | Preset type                                                                                                                                                                 | Have       | Textbox   | **Audio** | Disable does not allow editing.                                                                                                                                                          |
| Codec       | Use to compress and decompress audio or video data to reduce size and increase transmission capacity.                                                       | Have       | Select    | AAC       | Options: aac, ac3, eac3, mp2, copy<br />**With copy option not allowed to edit other configurations**                                                                                    |
| Audio rate  | The audio sample rate is transmitted in a unit of time, usually measured in Hz. It determines the quality and detail of the sound.          | Not        | Integer   | 64000     | 64000 <= birate <= 60000000                                                                                                                                                                              |
| Sample rate | The number of audio samples is taken in one second. It affects the quality and detail of the sound, which is measured in Hz.                | Not        | Select    | 44100     | 44100, 48000                                                                                                                                                                                             |
| Channel     | The number of audio channels transmitted.                                                                                                                   | Not        | Select    | Choose    | 1, 2, 6                                                                                                                                                                                                  |
| Profile     | A set of configuration parameters used to specify how video or audio data is encoded and decoded.                                                           | Not        | Select    | Choose    | aac_low, aac_he, aac_he_v2, aac_main, aac_ld, aac_eld |
| Volume      | Measure sound levels, adjust to be compatible with listeners' preferences or requirements.                                                                  | Not        | Select    | Choose    | +5dB, -10dB, 0.5, 2, loudnorm                                                                                                                                                            |
| Language    | The language used for audio or text content during streaming.                                                                                               | Not        | Select    | Language  | According to international standards                                                                                                                                                                     |
| Label       | Specification information used to classify or identify content. For audio, labels are applicable to genres like music, info, podcasts, etc. | Not        | Textbox   | Label     | N/A                                                                                                                                                                                                      |

### Data

Allows selecting the most **10 data**.

The user selects the 'audio' item, then displays the following information:

! [Data] (/images/media-live/profile/data.png)

| School name | Describe                                                                                                              | Compulsory | Data type | Default  | Rule                                             |
| ----------- | --------------------------------------------------------------------------------------------------------------------- | ---------- | --------- | -------- | ------------------------------------------------ |
| Kind        | Preset type                                                                                                           | Have       | Textbox   | **Data** | Disable does not allow editing.  |
| Codec       | Use to compress and decompress audio or video data to reduce size and increase transmission capacity. | Have       | Select    | Copy     | Options: scte35, id3, copy<br /> |

## Buttons

- 'Cancel' button: Do not perform new creation, return to the main screen interface.

- 'Confirm' button: Save the newly created information, return to the main screen interface.

## Save the configuration

**Step 5**: The user adjusts the parameters and clicks the 'Confirm' button at the bottom of the pop-up window.

The system will proceed to create a new profile with the information just entered and display a pop-up notification **Create new successful** at the top of the interface.

<!-- ![]() -->

At the same time, the basic information of the new profile will be displayed in the list of profiles. The new profile will appear in all profiles on the media live service that selected the profile.
