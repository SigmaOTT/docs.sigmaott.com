---
title: Input data
order: 2
---

# Basic configuration guide

## Input operations

A few notes, as well as general descriptive information when users add and edit data in the form:

<!--
- Giao diện:

- `Thông báo lỗi`: dữ liệu người dùng nhập trong form cần được kiểm tra lại để đảm bảo đúng định dạng, yêu cầu.

1. Trường dữ liệu không được bỏ trống -->

![Auto Refresh](/images/media-live/um-form-rules/required.png)

In a form will include multiple data fields, each data field will consist of 2 components: _Title_ and _Data input/selector_.

- The _title_ section displays the name information. The data field description information is displayed when the mouse pointer is moved to the ! [Info Icon] (/images/media-live/um-form-rules/info-icon.png).

  ![More Info](/images/media-live/um-form-rules/description.png)

  ***

  **\*Note**

  For data fields with icons <span style="color: #f43f5e;">\*</span> Previously, the data field must not be blank, forcing the user to enter data before saving the form.

  ***

- The _Data input/selection box_ section allows users to enter/select the desired data.

  User data sometimes needs to be validated to ensure validity, when the user data entered is invalid, there will be an error message **red** displayed just below.

  ![Error Msg](/images/media-live/um-form-rules/error-msg.png)

  The content of the error message depends on each specific case. Here are a few more types of notifications:

  ![Other Error Msg](/images/media-live/um-form-rules/error-msg-regex.png)

  ![Other Error Msg](/images/media-live/um-form-rules/error-msg-range.png)

  ![Other Error Msg](/images/media-live/um-form-rules/error-msg-enum.png)

## Submit data

When the user verifies the data stored in the form by pressing the **Submit** or \*\*Save \*\*\* button. The system executes the task and then returns a message to the user:

- If the execution is successful, a blue message will be displayed at the top of the browser screen.

  ![Error Notification](/images/media-live/um-form-rules/success-noti.png)

- If the execution fails, there will be a red message, with an error displayed at the top of the browser screen.

  ![Error Notification](/images/media-live/um-form-rules/error-noti.png)

When manipulating the funnel creation/editing form, the template will require many different data units, which are grouped into items in the form.

In the process of data processing system, in case an error appears, the items in the form that currently have errors will change to **red**, when clicking on those parts, the user will see error details.

! [msg] (/images/media-live/um-form-rules/transcode-modify.png)

! [msg] (/images/media-live/um-form-rules/transcode-detail-msg.png)

When manipulating the funnel/template creation/editing form, users need to perform many steps in turn to be able to complete the task.

For example, for creating a new channel, 2 main steps should be performed:

![Channel Steps](/images/media-live/um-transcode-forms/channel-step-01.png)

1. Select a channel type, including 2 types: _Create from scratch_ and _Create from template_.
   After the user completes **step 1** and clicks the ! [Next step button] (/images/media-live/um-transcode-forms/next-step-btn.png), all user data at this step will be recorded before moving to **step 2**.

2. Enter all required information.
   The interface as well as the data will be displayed depending on the options that the user has set from **step 1** before.

In step 2, there are a few options for users to navigate their data setup:

![Channel Redirection Options](/images/media-live/um-transcode-forms/channel-redirection-options.png)

- If the person clicks **Submit** there will be 3 more options after successful creation
  - 'Submit then stay' the user continues to stay on the current page and data is not lost.
  - 'Submit then back' the user will be redirected to the channel/template list page.
  - The 'Save as template' message is saved as a new template.

Alternatively, if you want to go back to **step 1** earlier, click the ! [Previous Button] (/images/media-live/um-transcode-forms/previous-btn.png). However, all currently entered data will be deleted, and the system also issues a message displayed in the middle of the screen for the user to confirm before performing.

! [Redirection Confirmation] (/images/media-live/um-transcode-forms/redirection-confirmation.png)

If you press 'OK', the interface will return to step 1 and all data is deleted.

If 'Cancel' is pressed, the system cancels the operation again.
