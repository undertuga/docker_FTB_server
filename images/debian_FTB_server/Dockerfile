# defining base image
FROM debian:latest

# defining image labels
LABEL "author"="undertuga <undertuga@protonmail.ch>"
LABEL "version"="1.0.0"
LABEL "description"="Debian Based | FTB Minecraft Server"

# exposing required tcp / udp ports
EXPOSE 25565

# updating and installing required packages on base system
RUN apt update && apt upgrade -y
RUN apt install build-essential vim htop netcat dnsutils net-tools wget default-jre default-jdk

# setting up FTB server install
RUN mkdir /var/FTB
RUN wget https://api.modpacks.ch/public/modpack/91/2085/server/linux -O /var/FTB/ftb_install
RUN chmod +x /var/FTB/ftb_install