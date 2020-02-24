FROM ruby

MAINTAINER hyshin <hyshin@student.hive.fi>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install nodejs -y && \
    gem install rails && \
    mkdir -p /opt/app
#make a folder, -p - make another folder inside of a new folder, /opt/app - name of the folders

ONBUILD WORKDIR /opt/app
ONBUILD ADD . /opt/app
ONBUILD EXPOSE 3000
ONBUILD RUN bundle install && rake db:from && rake db:to

#docker build -t ft-rails:on-build .
#docker run -it --rm -v "$PWD":/usr/src/app -w /usr/src/app rails:4 rails new --skip-bundle app
#docker build . -t ft-rails
#docker run -d -p 3000:3000 ft-rails
