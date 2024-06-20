# Menu And Navigator

There are multiple navigation options in the Controller. Some menu options depend on the version of Sigma OTT that you have installed.

## Home page and dashboard overviews

The Dashboard screen displays basic information, an overview of the services running on the system. Where:

1. Transcode state

Display service overview **Transcode & Package**

! [Transcode/packager Channel Status] (/images/media-live/um-dashboard/transcode.png)

2. Machine state

Display server-related information **Transcode & Package**

! [Server Status] (/images/media-live/um-dashboard/machine.png)

1. Origin state

Display information related to Origin system KPIs including:

- **Request Rate**: The rate of system requests

- **Response success rate**: Success / failure rate

- **Bandwidth**: The returned system bandwidth

- **quantile Response Times**: Provide the values **P99**, **P90**, **P50** corresponding to requests

- Note: Requests to Origin are divided into 2 types **segment** (Request for media- ts, m4v file), **manifest** (request for manifest file - m3u8, mpd)

! [System status origin] (/images/media-live/um-dashboard/origin.png)

## **Menu panel**

List of system features menus. This list will depend on the system feature pack you are provided with

! [Menu List] (/images/media-live/um-panel-menu.png) { width=150px }

## Breadcrumb

Breadcrumbs show links users have visited before. The breadcrumb content is displayed at the top of the browser screen.

![Breadcrumb](/images/media-live/um-breadcrumb/sample.png)

## Header Menu

![Header Menu](/images/media-live/um-header-menu/main.png)

Includes 3 options:

- Toggle full screen view on/off.
- Customize the font size.
- Manipulation of user accounts.

### Enable/disable full screen view

![Fullscreen Menu](/images/media-live/um-header-menu/fullscreen.jpg)

Allows users to enable/disable full screen view.

By default, this behavior is not enabled.

When activated, the app content will overflow to the entire screen.

### Customize font size

![Fontsize Menu](/images/media-live/um-header-menu/font-size.jpg)

Set the font size for the entire application.

Includes 4 options 'Default', 'Medium', 'Small' and 'Mini' corresponding to 4 sizes _Default_, _Medium_, _Small_ and _Very small_.

After selecting 1 of the 4 options above, the application font size will change accordingly.

### Follow the interaction with the user account

![Profile User](/images/media-live/um-header-menu/profile.jpg)&ensp;
![Home Profile User](/images/media-live/um-header-menu/home-profile.jpg)&ensp;
![Change Password Profile User](/images/media-live/um-header-menu/change-pwd-profile.jpg)&ensp;
![Logout Profile User](/images/media-live/um-header-menu/logout-profile.jpg)

Allows users to manipulate accounts after logging into the system.

Includes 4 options 'Home', 'Change password' and 'Log out'.

- 'Home' redirects the user back to **Home**.
- 'Change password' changes the user account password. This option will redirect the user to the **Change password** page.
- 'Logout' logs out of the current account and redirects the user to the **Login** page.

## List of managed servers

The **Server** section displays system information for monitoring and managing the server. The status of the server includes:

- **live**: The server is registered and still connected to the control system
- **dead**: The server is registered but no longer connected to the control system

The Sigma Transcoder system manages 2 types of servers:

- **Transcode**: Performs multimedia content transcoding tasks
- **Package**: Perform packaging tasks

! [Server classification] (/images/media-live/um-machine-tab.png)

On the system interface screen, you can list and monitor servers by different items:

! [Server List] (/images/media-live/um-machine-list.png)

Where:

| headline    | Describe                                                       |
| ----------- | -------------------------------------------------------------- |
| **#**       | Server sequence number                                         |
| **Machine** | Address of the registered server                               |
| **GPU**     | Does the machine use **GPU** or not                            |
| **CPU**     | The machine uses **CPU**                                       |
| **Task**    | The number of tasks being executed on the server               |
| **Speed**   | Lowest task execution speed on server (0-1) |
| **Percent** | %load of the server executing the task                         |
| **Ram**     | % Ram server in use                                            |
| **Status**  | Server status **live** or **dead**                             |
