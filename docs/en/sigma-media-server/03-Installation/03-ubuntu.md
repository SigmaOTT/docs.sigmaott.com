---
title: Install:Ubuntu
order: 3
---

# Install Sigma Media Server on Ubuntu

First, we will install Sigma Media Server. It is a powerful software application that allows you to stream video and audio over a network.

Example installation of version **sigma media server** **3.0.8** on ubuntu

```bash
 wget https://repo.sigma.video/debian/sigma-media-server.list -O /etc/apt/sources.list.d/sigma-media-server.list
 sudo apt-get update
 sudo apt-get install sigma-media-server
```

## Start Service

After a successful installation, you need to start the Sigma Media Server service:

```bash
sudo systemctl start sigma-media-server
```

## Register Server

Finally, you need to register your server with Sigma. You can do this by following the instructions here [register](./04-register.md)

Good luck in installing and using Sigma Media Server! If you face any problems, do not hesitate to contact us to get assistance. We're always happy to help you.
