# FTB Minecraft Server | Docker Implementation
Docker implementation of the Minecraft FTB Server (Debian based)
***

Just clone the rep, and then build the FTB Minecraft server image with the desired modpack (you will need the mod pack id).

In this example, we will boot up a FTB Minecraft server with the OceanBlock modpack (MOD_ID=91), ready to go:  


`docker-compose build --build-arg MOD_ID=91 ftb-server  `

`docker-compose up -d  `


- [Feed the Beast Website](https://feed-the-beast.com/)
- [Docker Website](https://www.docker.com)
- [Docker Compose Website](https://docs.docker.com/compose/)
- [Docker HUB Debian Oficial Image](https://hub.docker.com/_/debian)
