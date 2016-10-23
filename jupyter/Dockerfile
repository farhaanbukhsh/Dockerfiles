# Jupyter
# Build using: sudo docker build -t "python-tool:0.0.1" --rm=true --no-cache .
#
# NAME             python-tool
# VERSION          0.0.1
# LAST_UPDATED     2015-10-23 14:59

FROM ubuntu:16.04
MAINTAINER Farhaan Bukhsh "farhaan.bukhsh@gmail.com"

RUN apt-get update -y
RUN apt-get install -y python python-dev python-distribute python-pip
RUN pip install jupyter
RUN pip install ptipython

EXPOSE 8888

