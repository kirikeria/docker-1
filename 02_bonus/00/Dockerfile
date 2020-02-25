FROM ubuntu:latest
MAINTAINER hyshin <hyshin@student.hive.fi>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y nodejs git npm build-essential vim

RUN npm install npm --global

# https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/
# https://docs.npmjs.com/cli/install