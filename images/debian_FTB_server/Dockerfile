
# defining base image
FROM debian:latest

# defining image labels
LABEL "author"="undertuga <undertuga@protonmail.ch>"
LABEL "version"="1.0.0"
LABEL "description"="Debian Based | FTB Minecraft Server"

# exposing required tcp / udp ports
EXPOSE 25565
EXPOSE 19132

# updating and installing required packages on base system
RUN apt update && apt upgrade -y
RUN apt install -y wget default-jre default-jdk

# setting up & running FTB server install
ARG MOD_ID
RUN mkdir /var/FTB
RUN wget https://api.modpacks.ch/public/modpack/91/2085/server/linux -O /var/FTB/ftb_install
RUN chmod +x /var/FTB/ftb_install && chown -R 777 /var/FTB/ftb_install
RUN cd /var/FTB && ./ftb_install ${MOD_ID} --auto --verbose

# injecting previously accepted EULA
RUN echo "eula=true" > /var/FTB/eula.txt