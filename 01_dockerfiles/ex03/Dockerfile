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

# docker build -t ex03. 
# docker run --name ex03 -it --rm -p 80:80 -p 22:22 -p 443:443 --privileged ex03
# --privileged : Running a container with the --privileged flag gives all the capabilities to the container and also access to the host’s devices (everything that’s under the /dev folder).
# https://medium.com/better-programming/docker-tips-mind-the-privileged-flag-d6e2ae71bdb4
# In order to receive 
# https://gitlabfan.com/is-gitlab-incredibly-heavy-to-install-940fb70c3683
