# FTB Minecraft Server | Docker Implementation

![](https://s.softdeluxe.com/icons/png/128/6724/6724736.png)
![](https://forum.feed-the-beast.com/data/attachments/3/3788-1a52e7eaf3d905d43111cc5a0b463ec9.jpg)

Docker implementation of the Minecraft FTB Server (Debian based)
***

**Requirements:**
- Docker 👉 [Install Instructions](https://docs.docker.com/get-docker/)
- Docker Compose 👉 [Install Instructions](https://docs.docker.com/compose/install/) 

***

Just clone the rep, and then build the FTB Minecraft server image with the desired modpack (you will need the mod pack id).

In this example, we will boot up a FTB Minecraft server with the OceanBlock modpack (MOD_ID=91), ready to go:


***`export MOD_ID=91 && docker-compose up --build -d `***

After that, you should have a fully functional and ready to go server!  
⚠️ Make sure that port ***25565/tcp*** is open on your firewall. ⚠️

Run ***`docker ps -a `*** to check your container status.

To access the container, just run ***`docker exec -it [container-name] bash`***.

Feel free to edit the **server.properties** file locate at **images/debian_FTB_server/server.properties**.

***

- [Feed the Beast Website](https://feed-the-beast.com/)
- [Docker Website](https://www.docker.com)
- [Docker Compose Website](https://docs.docker.com/compose/)
- [Docker HUB Debian Oficial Image](https://hub.docker.com/_/debian)
