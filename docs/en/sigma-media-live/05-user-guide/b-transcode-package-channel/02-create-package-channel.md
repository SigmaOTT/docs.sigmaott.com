---
title: Create packing funnels
order: 2
---

# {{ $frontmatter.title }}

The package prepares and protects your video for distribution over the Internet through multimedia data transmission formats via http (HTTP Adaptive Stream) protocols such as HLS, DASH

To create a manually packaged channel, perform the basic funnel creation steps. Please select according to the instructions

- **Manual** => **Package** => **Next**

The interface screen for configuring the packaging channel appears as follows:

! [Create a manually packaged channel] (/images/media-live/um-create-channel/um-create-package-channel-1.png)

In which the menu bar on the right will have the following items:

1. **Config**: Basic configuration of the channel

2. **Inputs**: Input flow configuration

3. **Profiles**: List of profiles used

4. **Targets**: Configure the list of desired outputs (HLS/DASH... )

::: tip

- For the packaging channel, the system will automatically configure **Profile** corresponding to **Input** added. So you just need to add **Input** values, **Profile** values will be added automatically and you do not have permission to change these values
  :::

## B1. General Configuration

In the basic packaging channel configuration is divided into the following items:

- **Information**:
  - **Name**: The name of the channel used to distinguish and search for channels in the channel list
  - **Description**: Channel description
  - **Tags**: List of tags
- **Name modifier**: The alternate name of the channel must be unique throughout the system, serving to query the manifest 1 file briefly

:::tip
For example, if the alternate name is **VTV1**: the manifest access link will look like this: _http://origin/com/manifest/VTV1/manifest_name_
:::

- **Options**: Advanced configuration of the channel

## B2. Channel input configuration

Select the Plus button to add inputs to the channel. The input list for the listed Package channel will appear. Please select the input for the desired channel

For each element in the input list of the input, the system will automatically create 1 corresponding profile, with an alternate name installed when creating the input

:::info
This alternative name helps the system define the desired profile name for the ABR profile set. For example, with the input stream **1080p** you should alternate the profile as **1080p**, this alternative name will be in the path of the manifest file corresponding to the profile to be packaged
:::

## S3. Channel Encapsulation Output Configuration

Select the 'Plus' key under 'Target' to add 1 desired output. A popup displaying the desired outputs will appear. The system supports the following outputs:

- **HLS**: Apple Http Live Streaming
- **DASH**: DASH
- **UDP**: multicast or unicast mpeg transport stream
- **RTMP**: Realtime Message Protocol

After initializing 1 desired output. The configuration of the output will appear as follows. Where:

- **Data**: Basic configuration of output
  - **Name**: The name of the output
  - Replaced name: The name added to the end of the source manifest file, which must be unique to different outputs of the same type HLS or DASH, serves to create a unique path for HLS or DASH manifest files, should be preceded by a "_" or "-". Can be left "empty" if you want to preserve the source manifest filename
    - For example, if you leave it empty, the source manifest file of HLS would be named **master.m3u8** with Dash as **master.mpd**
    - For example, if you set it to "**-tv360**, the source manifest file of HLS would be named **master-tv360.m3u8** with Dash as **master.mpd**
  - **Format**: The name of the output type
  - **Description**: Output description

- **Manifest**: Configure **manifest** and **segment** files
  - **Container**: **segment** file format. Has a value of **mpeg-ts** or **fmp4**. The default is **mpeg-ts**
  - **TS**: The length of 1 **segment** file. The default is 6 seconds
  - **Counter**: Number of Segment files saved in **manifest** file
  - **Time**: toggle display tag: **Programing-date-time** used with HLS output

- **DRM**: Configure DRM encryption
  - **Enable**: Configure DRM toggle
  - **Key provider**: A method of providing an encryption key, static or obtained from the server containing the encryption key
    - **static**: static encryption key
    - **sigma-drm**: Sigma Drm encryption system
    - **Sigma-drm-v1**: Sigma DRM V1 Encryption System
    - **Sigma-multi-drm**: Multi-DRM encryption system supporting Widevine, PlayReady, FairPlay implemented by Sigma drm
    - **drmtoday**: Multi-DRM encryption system supporting Widevine, PlayReady, FairPlay implemented by castlab
  - Set 'DRM Credential' if any for 'Sigma Multi DRM' 'DRMtoday'

- **Low Latency**: Low Latency TV Configuration

- **Catchup**: Catchup-timeshift Storage Configuration

  - **Storage**: Turn catchup-timeshift storage mode on and off
  - **Cache time**: Configure the desired unit storage time in hours
  - **Trickplay**: Toggle Trickplay mode on and off with catchup

- **Startover**: Toggle 'Startover' storage mode on and off

- **Preset**: Configure profiles packed into this output

### Instructions for configuring **preset** with output:

1. choose! [select profile] (/images/media-live/um-create-channel/um-select-profile.png) { width=100px } to select the profiles that will be encapsulated in this output. The profile list panel will be displayed
2. Check the box to select the **profile** you want to add to the output => click **submit** to complete the operation
3. The list of selected profiles will appear, you can manipulate the desired tasks for this list such as adding, deleting, editing

## B4. 'Submit' Save channel

After saving the channel, the system will automatically 'start' the channel and its outputs corresponding to each target
