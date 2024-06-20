---
title: Create a new event channel
order: 1
---

# Create a new event channel

This function allows CMS to create a new event channel, to create an event channel, we perform the basic funnel creation steps.

## Step 1: Set up the global configuration

At the Event channel main screen interface, users click on the "Create new channel" button

Screen system **Configuration settings for Event Channel**, general configuration settings for Event channel

! [General Configuration Settings] (/images/media-live/event-channel/create-event-channel-1.png)

[](.. /d-input-management/d-duplicate-input.md#create-input)

With the main information:

- **Information**:
  - **Name**: The name of the channel used to distinguish and search for channels in the channel list (requires entry, up to 50 characters)
  - **Description**: Channel description (no input required, maximum 200 characters)
  - **Tags**: List of tags (up to 100 tags, each tag entering up to 35 characters)
  - **Create MP4**: toggle button to mark the channel on/off MP4 creation

- **Interactive**: Display configuration at the product **_Tương tác_**

- **Watermark**: Configure enable/disable marking of images to the video screen (watermark position preview supported) Add up to 10 watermarks.

  When users **_Bật watermark_**, there are 2 ways users can use drag / drop on watermark on the preview screen, the parameters of X and Y coordinates will be automatically displayed respectively, and **vice versa** when filling in X and Y coordinates, the watermark will be displayed on the corresponding preview screen

  - **Latency(s)**: Delay of watermark
  - **X**: X coordinates (width of screen)
  - **Y**: Y coordinates (vertical of the screen)

  Add bookmarked images by clicking the dung__Chọn button to upload or pre-select from the system's library

- **Blackout**: when the signal is lost, the screen will display the uploaded content in the configuration (users can choose to turn it on or off)

## Step 2: Set up Input

After the user has filled in the required information, press the "Next" button, the system switches to the Input Setup screen

Users need to configure for 3 event timelines: _**Pre-Event, Main-Event, Post-Event**_

Display event timeline, displayed according to the user's configuration:

- **Start-Pre** (yyyy/mm/dd HH:MM:SS): Displayed in the timeline when the user has finished selecting and Start-Pre is in _**enabled**_

- **Start-Main** (yyyy/mm/dd HH:MM:SS): Always on and always displayed in the time bar when the user is done with the operation

- **End-Main** (yyyy/mm/dd HH:MM:SS): The End-Main moment will automatically be calculated as "Start-Main Moment" + "Total duration of added assets".

- **End-Post** (yyyy/mm/dd HH:MM:SS): calculated using the following formula End-Post = End-Main + Time for Post-Event

In between each event, the system calculates the total amount of time between the two events so that the user has more information.

### Pre-Event Configuration Settings

! [Pre-Event Configuration Settings] (/images/media-live/event-channel/create-event-channel-pre-event.png)

The user can enable or disable the setting for Pre-Event, if **enabled** the user must provide the following information to complete the setup:

- **Start Pre**: is the start time of the Pre-Event. Allow users to choose the Pre-Event start date and time (Pre-Event must be at least 5 minutes and maximum 7 days)

- **Input**: The user selects the input of photos or videos from the gallery or uploads new content (only select 1 is allowed)

- **Countdown**: countdown events

### Main-Event Configuration Settings

! [Main-Event Configuration Settings] (/images/media-live/event-channel/create-event-channel-main-event.png)

Mandatory user to configure Main-Event

- **Start Main**: is the start time of the Main-Event (Main-Event must have a minimum duration of 5 minutes and a maximum of 2 days)

- **End Main**: The End-Main time depends on the selection **Input**
  - When the input selection is ASSET\*\*\*: The End-Main time will automatically be calculated as "Start-Main time" + "Total duration of added assets"

  - When the input selection is INPUT\*\*\*: End-Main time the user will be selected (Main-Event must have a minimum duration of 5 minutes and a maximum of 2 days)

- **Input**: Users can choose 2 types: _**INPUT**_ and \***ASSET**
  - For type **INPUT**\* allow option 1 (can be selected from the input list or created new)
  - For _**ASSET**_ allows a minimum selection of 1 and a maximum of 50 (can choose from the library or load a new file)

### Post-Event Setup

! [Post-Event Configuration Settings] (/images/media-live/event-channel/create-event-channel-post-event.png)

The user can enable or disable the setting for Pre-Event, if **enabled** the user must provide the following information to complete the setup:

- **Post-Event Interval**: is the catch time for Post-Event. Allow users to choose from a list of times 00:05 -> 23:55 (minutes)

- **Input**: The user selects the input of photos or videos from the gallery or uploads new content (only select 1 is allowed)

## Step 3: Set up your profile

After the user has filled in the required information, press the "Next" button, the system switches to the Profile Setup screen.

! [Profile Setup] (/images/media-live/event-channel/create-event-channel-profile.png)

The system displays 4 profiles by default with default settings.

Users can set up to 20 profiles for the channel (can choose from the existing list or create a new one)

## Step 4: Set Goals

After the user has filled in the information in the **Set up profile** section, click the "Next" button, the system switches to the Profile Setup screen.

! [Goal Setting] (/images/media-live/event-channel/create-event-channel-target.png)

Select the **Add**\* key in the **Target** field to add 1 desired output. A popup displaying the desired outputs will appear. The system supports the following outputs:

- **HLS**: Apple Http Live Streaming
- **DASH**: DASH
- **UDP**: multicast or unicast mpeg transport stream
- **RTMP**: Realtime Message Protocol
- **Mss**: Maximum Segment Size
- **Hds**: HTTP Dynamic Streaming

After initializing 1 desired output. The configuration of the output will appear as follows. Where:

**Data**: Basic configuration of output

**Manifest**: Configure **manifest** and **segment** files

- **Container**: **segment** file format. Has a value of **mpeg-ts** or **fmp4**. The default is **mpeg-ts**

- **TS**: The length of 1 **segment** file. The default is 6 seconds

- **Counter**: Number of Segment files saved in **manifest** file

- **Time**: enable/disable insert timestamp into playlist
  **Playlist** enable/disable insertion timestamp into playlist

- **DRM**: Configure DRM encryption
  - **Enable**: Configure DRM toggle

  - **Key provider**: A method of providing an encryption key, static or obtained from the server containing the encryption key

    - **static**: static encryption key
    - **sigma-drm**: Sigma Drm encryption system
    - **Sigma-drm-v1**: Sigma DRM V1 Encryption System
    - **Sigma-multi-drm**: Multi-DRM encryption system supporting Widevine, PlayReady, FairPlay implemented by Sigma drm
    - **drmtoday**: Multi-DRM encryption system supporting Widevine, PlayReady, FairPlay implemented by castlab

  - Set up **DRM Credential** if applicable for **Sigma Multi DRM** and **DRMtoday**

## Step 5: Confirm Preview and complete channel creation

After completing all the above steps, the user presses the **Next** button, the system displays the Preview screen including the information configured in the previous steps, so that the user can check the content before completing the channel creation step.

! [Preview Confirmed] (/images/media-live/event-channel/create-event-channel-preview.png)

After double-checking the information, the user clicks the **Confirm** button to complete the event funnel creation step. Once a new event channel is successfully added, it will show up in the event channel list
