FROM debian
MAINTAINER hyshin <hyshin@student.hive.fi>

ENV TS3SERVER_LICENSE=accept

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install curl bzip2 apt-utils -y &&\

#PORT
EXPOSE 9987/udp 10011 30033

RUN useradd ts3
WORKDIR /home/ts3

RUN curl http://dl.4players.de/ts/releases/3.8.0/teamspeak3-    server_linux_amd64-3.8.0.tar.bz2 > teamspeak.tar.bz2 \

RUN tar -xjvf teamspeak.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
USER ts3
ENTRYPOINT sh ts3server_minimal_runscript.sh

# http://dl.4players.de/ts/releases/
# https://www.tecmint.com/18-tar-command-examples-in-linux/
# https://forum.teamspeak.com/threads/132611-Install-teamspeak-3-server-on-Debian-8
#docker build -t ex01. 
#docker run -it --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
