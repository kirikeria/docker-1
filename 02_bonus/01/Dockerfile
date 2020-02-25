FROM ubuntu
MAINTAINER hyshin <hyshin@student.hive.fi>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y default-jre wget

WORKDIR minecraft

RUN wget https://launcher.mojang.com/v1/objects/3737db93722a9e39eeada7c27e7aca28b144ffa7/server.jar -O minecraft_server.1.13.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

CMD java ‑Xms512m ‑Xmx1024m ‑jar minecraft/minecraft_server.jar nogui

# https://www.linode.com/docs/game-servers/how-to-set-up-minecraft-server-on-ubuntu-or-debian/
# https://developer.ibm.com/technologies/containers/tutorials/minecraft-and-ibm-cloud-part-1/
# https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-debian-10