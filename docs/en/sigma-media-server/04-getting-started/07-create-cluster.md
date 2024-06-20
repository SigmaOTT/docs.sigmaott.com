---
title: Create a new Cluster
order: 7
---

## Create a new Cluster Server

Creating cluster servers helps users to group machines together into a cluster, making it easier to support each other to handle tasks between machines. Specifically, the combined machines can support each other in the event of a machine death or malfunction.

Help improve work speed and efficiency, while minimizing the risk of data loss and ensuring the continuity of job processing processes.

Users can create a new Cluster Server by following these steps:

1. Access the Cluster Server management section with the type of machine you want to add

2. Click "Add new server cluster"

3. In the server cluster configuration form, users perform configuration with the following information:
   ! [Create Cluster] (/images/media-server/getstarted/create-cluster.png)
   ! 

   1. Cluster name.

   2. Describe.

   3. Ingest configuration: Users can enter RTMP Public URI/ SRT Public URI / Web RTC Public URI addresses.

   4. Add machines: Users can add the desired machines in clusters here.

      For the machine environment, the user needs to select the machine, enter the IP address of the machine, enter the routing prefix.

      :::tip Each machine can only add to one Cluster Server. :::

   5. Origin configuration: The user enters the HTTP public URI address.

4. After configuring and checking the information, users click "Send" to add Cluster Server

More successfully, the Cluster Server is ready for users to use.
