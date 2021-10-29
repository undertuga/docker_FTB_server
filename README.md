# FTB Minecraft Server | Docker Implementation
Docker implementation of the Minecraft FTB Server (Debian based)
***

Just clone the rep, and then build the FTB Minecraft server image with the desired modpack (you will need the mod pack id).

In this example, we will boot up a FTB Minecraft server with the OceanBlock modpack (MOD_ID=91), ready to go:


`export MOD_ID=91 && docker-compose up --build -d `

After that, you should have a fully functional and ready to go server!
Remenber to make sure that port 25565/tcp is open on your firewall.

Run `docker ps -a ` to check your container status.

To access the container, just run `docker exec -it [container-name] bash`.

Feel free to edit the *server.properties* file locate at *images/debian_FTB_server/server.properties*.

- [Feed the Beast Website](https://feed-the-beast.com/)
- [Docker Website](https://www.docker.com)
- [Docker Compose Website](https://docs.docker.com/compose/)
- [Docker HUB Debian Oficial Image](https://hub.docker.com/_/debian)
