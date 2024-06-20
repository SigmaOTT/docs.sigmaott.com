---
title: Create new input
order: 1
---

# Create new input

The Input Management feature helps users manage input data more efficiently and easily. Users can add, edit, and delete inputs, creating input data records. Each input created can add 1 machine or 1 specific cluster, which is convenient for coordinating and processing jobs when the channel is created.

There are 2 types of input: Transcode channel input and Package channel input

## Create new Transcode channel input

This function allows CMS users to create new Transcode type inputs

**Step 1**: To access the Media Live product, the user selects the Inputs tab.

The system displays by default with the Transcode tab, the Transcode type input list screen interface.

! [Create new Transcode channel input] (/images/media-live/input/create-transcode-input.png)

**Step 2**: At the Transcode Input list screen interface (Transcode tab), the user clicks the **Add** button

The system displays a pop-up that adds new Transcode input on the right side of the screen.

With general information:

| Name                  | Function                                                                                                                                                                   |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**              | Name of Transcode input                                                                                                                                                    |
| **Describe**          | The description of Transcode Input App                                                                                                                                     |
| **Based on Machine**  | Enable Based on machine activation                                                                                                                                         |
| **Kind**              | Types of input sources include UDP, RTMP_PUSH, RTMP_PULL, SRT_PUSH, SRT_PULL, HLS, SDI |
| **Machine type**      | Type of machine to use includes: Sigma Machine, Sigma Machine cluster, Sigma Component Cluster                                                             |
| **Machine**           | The specific machine is suitable for performing the task                                                                                                                   |
| **Redundancy**        | Input Class: _**Single**_ (1 main input source), _**Redundancy**_ (Main input source + secondary input source)       |
| **Primary source**    | Main input source information                                                                                                                                              |
| **Secondary sources** | 2nd input source information (Select **Secondary source** if **Type** is UDP, RTMP Pull, SRT Pull)                                                      |

- The information for the type of the input source is UDP (Type field = "UDP"):

| Name                            | Function                                                                                            |
| ------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Primary Network Interface**   | Main Network Interface for UDP type input source                                                    |
| **Secondary Network Interface** | Network interface secondary to UDP type input source, allowing input when Input Class is Redundancy |

- **Cancel** button: Cancel the operation of adding new Transcode input
- **Reset** button: Reset all entered data, form back to default
- Button **Confirm**: Confirm saving the configuration of Transcode Input

**Step 3**: User enters the necessary information

**Step 4**: Once done, click the **Confirm** button at the bottom of the pop-up window.

The system creates a new Transcode input with the newly entered information, displaying a Pop-up message **Create Transcode input successful** in the middle of the screen to notify that the creation process has been successfully performed.

## Create New Package Input

This function allows CMS users to create new Transcode type inputs

**Step 1**: To access the Media Live product, the user selects the Inputs tab.

Here the system is displayed by default with the Transcode tab, the user selects the Package tab to switch to the Package type input list screen interface.

**Step 2**: At the Package Input list screen interface (Package tab), the user clicks the **Add** button

The system displays a pop-up that adds new Package input on the right side of the screen

! [Create new input channel Package] (/images/media-live/input/create-package-input.png)

With general information:

| Name                  | Function                                                                                                                                                             |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**              | Name of Package input                                                                                                                                                |
| **Describe**          | The description of Input Package App                                                                                                                                 |
| **Based on Machine**  | Enable Based on machine activation                                                                                                                                   |
| **Kind**              | The type of input source includes UDP, RTMP_PUSH, RTMP_PULL, SRT_PUSH, SRT_PULL  |
| **Machine type**      | Type of machine to use includes: Sigma Machine, Sigma Machine cluster, Sigma Component Cluster                                                       |
| **Machine**           | The specific machine is suitable for performing the task                                                                                                             |
| **Redundancy**        | Input Class: _**Single**_ (1 main input source), _**Redundancy**_ (Main input source + secondary input source) |
| **Primary source**    | Main input source information                                                                                                                                        |
| **Secondary sources** | 2nd input source information (Select **Secondary source** if **Type** is UDP, RTMP Pull, SRT Pull)                                                |

- The information for the type of the input source is UDP (Type field = "UDP"):

| Name                            | Function                                                                                            |
| ------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Primary Network Interface**   | Main Network Interface for UDP type input source                                                    |
| **Secondary Network Interface** | Network interface secondary to UDP type input source, allowing input when Input Class is Redundancy |

- **Delete** button at sources: Allows deleting added sources
- **Cancel** button: Cancel the operation of adding new Transcode input
- **Reset** button: Reset all entered data, form back to default
- Button **Confirm**: Confirm saving the configuration of Transcode Input

**Step 3**: User enters the necessary information

**Step 4**: Once done, click the **Confirm** button at the bottom of the pop-up window.

The system creates a new Package input with the newly entered information, displaying a Pop-up notification **Create Package input successful** in the middle of the screen to announce that the creation process has been successfully performed.
