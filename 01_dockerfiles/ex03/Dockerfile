FROM ubuntu

MAINTAINER hyshin <hyshin@student.hive.fi>

RUN apt-get update -y && apt-get -y upgrade && apt-get -y install wget openssh-server \
	ca-certificates postfix

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && \
	chmod 777 ./script.deb.sh && \
	./script.deb.sh

RUN apt-get install -y tzdata gitlab-ce

EXPOSE 443 80 22

RUN gitlab-ctl reconfigure

# Build Image
# docker build -t ex03 .

# Create Container
# docker run --name ex03 -it --rm -p 80:80 -p 22:22 -p 443:443 --privileged ex03