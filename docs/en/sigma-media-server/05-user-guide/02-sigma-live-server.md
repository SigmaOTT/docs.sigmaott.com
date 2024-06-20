---
title: Sigma Media Server
order: 2
---

With the Sigma Live Server type, the type of machine that helps handle the Live channel stream. Users can create and configure with three types of machines:

[TEST]

## Máy Sigma Live Server:

Fully functional version machine, users have the ability to use with all the features provided by us with this type of machine.

Actions users can perform include:

### 1. Add Server

Users can add new machines, following these steps:

1. At the Sigma Live machine list screen, click **Add Server**

   ![add sever](/images/media-server/user-guide/add-server-1.png)

2. Perform to get the token to install the machine

   [Get token] (/en/sigma-media-server/03-getting-started/04-install-new-machine#lay-code-token-to-implement-install-machine)

3. Server settings

   [Install Server] (.. /03-getting-started/04-install-new-machine#implement-set-machine)

------

### 2. Drain Job

The function gives the user the ability to perform the **Drain Job** action, when the machine is asked to perform **Drain Job** the machine will eject all the Jobs being processed in that machine. Users can perform Drain Job in simple steps:

1. At the machine management screen, click **Drain Job** at the machine in the operating state (Running/ Paused)

   ! 

2. Click Confirm action execution

   ! 

The system will handle pushing all the jobs being done in the machine out

----

### 3. Pause/ Resume

Allows users to perform Pause/Restore machine operation. The user performs the steps:

1. At the machine management screen, click **Pause** at the machine in Running state

   ! 

2. Click Confirm action execution

   ! 

The machine will return to the "Paused" state

With the machine in the **Pause** state, the user wants to perform **Resume** to restore the operation of the machine. Follow the same steps:

1. At the machine management screen, click **Resume** at the machine in Paused status

   ! 

2. Click Confirm action execution

   ! 

The machine will return to the "Running" state

------

### 4. Config Route

The Config Route feature allows users to configure URI addresses so that the system can route and connect to Ingest and Origin addresses.

The system provides an interface that allows users to configure routing, including information:

- Ingest Configuration: Users can configure RTMP Public URI, SRT Public URI, Web RTC Public URI addresses
- Origin Configuration: Users can configure the HTTP Public URI address

To implement the Config Route, the user performs the following steps:

1. At the server list screen, click the **Config Route** action
   ! 

2. Configure the required information into the configuration form
   ! 

------

### 5. Add license

When the installation of the machine is successful, the user needs to assign a license to the machine to activate the operation.

With adding licenses users can do it in 2 ways:

##### Method 1: Go to Manage licenses

Perform the manipulations:

1. Click "Add license".

! 

2. Select the license type (Note: The activation usage license for the machine must be of the same type as the machine)
   ! 

3. Check the license information
   ! 

4. Make payment of the first bill of the license
   ! 

   ::: warning

   The license is usable when paid in advance.

5. Payment confirmation

6. System successfully billed license will be available

7. Click the "Use" action
   ! 

8. Select the machine to activate the operation
   ! 

9. Confirm license usage
   ! 

The license has now been successfully assigned to the machine, the machine is ready to receive jobs for processing.
:::Tip
If you already have a license in an "Available" status, you can perform "Use" the license immediately (Done from step 7).

##### Method 2: Access the Server Management section

Users can perform "Add License" directly to the server by following the steps:

1. For newly installed machines that have not been assigned a license, click the "Add License" action
   ! 

2. Users can do:

   ! 

   - **Select available license**: In case the application already has a license of the same type as the machine in the "Avaiable" state.
     ! 

   - **Option to add new license**: Users perform the steps to add licenses such as steps 2, 3, 4, 5, 6 at **Method 1**. After the license is successfully paid, the license will automatically be selected as the license to use for machine activation

     ! 

-----

### 6. Config App

The **Config App** function allows users to perform gateway configuration for Ingest and Origin servers.

Steps to perform application configuration:

1. Click **Server Name** to view server details
   ! 

2. In the App configuration information section, click **Config**

! 
3. Perform the configuration and confirm saving the configuration

- Ingest Configuration: Users can configure connection ports for RTMP Server, SRT Server, Web RTC Server
  ! 

- Origin Configuration: Users can configure the connection port for HTTP Server! 

------

### 7. Actions to App

In addition to configuring the App, users can perform **Start/ Stop/ Reset** application actions. Help handle cases where the application crashes or the user's desire to restart the application.

Users can perform actions in the following simple steps:

1. Access to view server details, at App configuration
2. Click the action button **Start/ Stop/ Reset** the application you want to perform

! 

------

### 8. Delete Server

With machines in **DEAD/ FREEZED** state, users can perform Machine Wipe, helping to remove machines that are no longer in use to ensure easier machine management. Users use the **Delete** button with DEAD/ FREEZED machines
! 

------

## Sigma Live Server Community Machine

Sigma Live Server Community is a free-to-use community machine edition that allows users to use some of the basic features of Sigma Live Server without paying.

With the community machine type, users do not need to perform a license assignment for the machine. The system will automatically create and assign free licenses for users to use.

Users are still allowed to perform all other functions with this machine similar to normal Sigma Live machines

### 1. Add Server

Users can add new machines, following these steps:

1. At the Sigma Live Community machine list screen, click Add Server

2. Perform to get the token to install the machine

   [Get token] (/en/sigma-media-server/03-getting-started/04-install-new-machine#lay-code-token-to-implement-install-machine)

3. Server settings
   [Install Server] (/en/sigma-media-server/03-getting-started/04-install-new-machine#with-server-community)

----

### 2. Drain Job

User performs action [Drain Job](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_2-drain-job)

----

### 3. Pause/ Resume

User performs action [Pause/ Resume](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_3-pause-resume)

----

### 4. Config Route

User performs action [Config Route](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_4-config-route)

------

### 5. Config App

User performs action [Config App](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_6-config-app)

-----

### 6. Actions to App

User performs action [Action to App](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_7-actions-to-app)

-----

### 7. Delete Server

User performs action [Delete Server](/en/sigma-media-server/04-user-guide/02-sigma-live-server#_8-delete-server)

## Cluster Server

The system provides a solution to help users group machines together into a cluster, making it easier to support each other to handle tasks between machines. Specifically, the combined machines can support each other in the event of a machine death or malfunction.

Help improve work speed and efficiency, while minimizing the risk of data loss and ensuring the continuity of job processing processes.

### 1. Add Cluster Server

User performs action [Add Cluster](/en/sigma-media-server/03-getting-started/07-create-cluster#create-moi-cluster-server)

----

### 2. Edit Cluster Server

Users are allowed to make modifications to the configuration of the server cluster, change the configuration or change the machine components in the cluster

----

### 3. Delete Cluster Server

Users can delete the cluster that no longer needs to be used by the action **Delete** in the Cluster Server management section

-----

### 4. View Logs

The system gives users the function to view the operation log of the server cluster. Each cluster will have an interface that displays the entire activity log of all servers located in the cluster.

Users can view a list of cluster activity logs by clicking the **View Logs** action in the Cluster Server management section.
