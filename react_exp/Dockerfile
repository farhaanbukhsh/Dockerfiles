# React Experimentation
# Build using: sudo docker build -t "react-exp:0.0.1" --rm=true --no-cache .
#
# NAME         react-exp
# VERSION      0.0.1
# LAST_UPDATED 2016-10-23 14:35

FROM       ubuntu:14.04
MAINTAINER Farhaan Bukhsh "farhaan.bukhsh@gmail.com"
 
RUN apt-get update && apt-get -y install wget
RUN wget "http://nodejs.org/dist/v4.6.1/node-v4.6.1-linux-x64.tar.gz"
RUN tar -xzvf node-*.tar.gz
RUN rm node-*.tar.gz
RUN mv node-* /opt/node
RUN echo 'export PATH=$PATH:/opt/node/bin/' >> ~/.bashrc
RUN ln -s /opt/node/bin/* /bin/

CMD    ["/opt/node/bin/node"]

RUN apt-get update && apt-get upgrade -y && apt-get -y install build-essential
RUN npm install -g jasmine grunt-cli webpack webpack-dev-server nodejs-config

EXPOSE 3000
