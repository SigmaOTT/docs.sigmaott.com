---
title: Create a folder tracking mechanism
order: 1
---

# Create a watch folder rule

This function allows users to create conditions for tracking folders. Any file uploaded that complies with the conditions described in this directory will automatically trigger transcoding

Each machine can only create a maximum of 10 directory monitoring mechanisms

To create a directory tracking mechanism, perform the following steps:

## **Step 1:** Access Media VOD products

To access the Media VOD product, users select **Watch folder** on the menu tab bar

The system displays the screen interface **List of folder rules** available

## **Step 2:** Fill in the general information of the watch folder rule

At the folder rules list screen interface, the user clicks the **"Add" button**

The system displays a pop-up window Create a new watch folder rule, with the following information:

- **Name**: Name of folder rule (required filling)

- \*\*"Cancel" button: when the user presses this button, the system will return to the Folder Rule List screen

- \*\*"Confirm" button: when the user clicks this button, the system will display the Create new watch folder rule screen

Users fill in the required information at the pop-up, then click the **"Confirm"** button at the bottom of the pop-up window

The system displays the Create new watch folder rule screen with input selection step

## **Step 3:** Select machine and folder

The user clicks on the input selection, the system displays a pop-up window, with the following information:

- **Machine:** select machine to perform file selection
- **Folder:** After selecting the machine, the system displays the folders corresponding to the machine (only folder selection is allowed)

## **Step 4 (optional):** Description of folder tracking conditions

After completing the selection of machines and folders to monitor, the system displays the items to select

The condition selection item (describes the condition for tracking the folder), when clicked on the system displays a pop-up window with the following information:

| **Column name**                       | **Describe**                                                                                                                                                                                                        | **Request**                                                            |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **regex pattern**                     | Provides the ability to search, match, extract and replace character strings based on a descriptive rule (condition) to find the format of the file then trigger automatically to create the job | Not required to fill, enter the allowed characters of the regrex       |
| **Bitrate (mpbs)** | Used to measure the data transfer rate or bitrate in a data stream                                                                                                                                                  | Optional, only numeric characters are allowed                          |
| **Width (px)**     | The width of the video frame                                                                                                                                                                                        | Optional, only numeric characters are allowed                          |
| **Height (px)**    | The height of the video frame                                                                                                                                                                                       | Optional, only numeric characters are allowed                          |
| **FPS (fps)**      | Frame rate per second                                                                                                                                                                                               | Optional, only numeric characters are allowed                          |
| **Size (byte)**    | Size of the video                                                                                                                                                                                                   | Optional, only numeric characters are allowed                          |
| **Duration(s)**    | Video encoding duration                                                                                                                                                                                             | Optional, only numeric characters are allowed                          |
| **Codec**                             | Transcoder                                                                                                                                                                                                          | Optional, the following options allowed: **H264, H265, AV1, VP9, VP8** |

- Button **"Next"**: the system switches to the next condition selection screen
- **"Previous"** button: the system returns to the regular expression filling screen
- Button **"Apply"**: The system saves information, displays the new creation screen

## Step 5: Select a destination

The system supports places to store output files, including: Storage at libraries, archive folders, third-party memory

See more at: [Select output (destination)](.. /b-job-management/1-create-job.md#step-3-select-head-out-destination)

## Step 6: Configure the job

The system supports selecting available templates or can create the desired configuration

See more at: [Job configuration](.. /b-job-management/1-create-job.md#step-4-shape-job)

## Step 7: Finish creating folder rules

At the last step, the user can edit the name of the rule

- \*\*"Create rule" button: The system performs directory tracking mechanism, displayed first on the top of the folder rules list

- **"Save sample"** button: The system saves the sample information of the job configuration. See more at:

The user presses the "Create rule" button, the system creates a new rule, displaying the message **Rule created successfully!** in the middle of the screen to notify that the creation process has been successfully executed.