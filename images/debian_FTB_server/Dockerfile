
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
RUN apt install -y build-essential vim htop netcat dnsutils net-tools wget default-jre default-jdk

# setting up & running FTB server install
ARG MOD_ID
RUN mkdir /var/FTB
ADD ./ftb_install /var/FTB/ftb_install
RUN chmod +x /var/FTB/ftb_install && chown -R 777 /var/FTB/ftb_install
RUN cd /var/FTB && ./ftb_install ${MOD_ID} --auto --verbose

# injecting previously accepted EULA
RUN echo "eula=true" > /var/FTB/eula.txt