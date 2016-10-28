# Pagure
# Build using: sudo docker build -t "pagure:0.0.1" --rm=true --no-cache .
#
# NAME         pagure
# VERSION      0.0.1
# LAST_UPDATED 2016-10-28 14:47

FROM fedora:latest
MAINTAINER Farhaan Bukhsh <farhaan.bukhsh@gmail.com>

RUN dnf -y update && dnf clean all
RUN dnf install -y make automake gcc gcc-c++ kernel-devel
RUN dnf install -y python2-devel python-setuptools python-nose py-bcrypt python-alembic \
                   python-arrow python-binaryornot python-bleach python-blinker \
                   python-chardet python-cryptography python-docutils python-flask \
                   python-flask-wtf python-flask-multistatic python-markdown python-psutil \
                   python-pygit2 python-pygments python-fedora python-openid python-openid-cla \
                   python-openid-teams python-straight-plugin python-wtforms python-munch \
                   python-enum34 python-redis python-sqlalchemy systemd gitolite3

RUN dnf install -y python-fedora-flask python-mock
COPY . /pagure
WORKDIR /pagure

EXPOSE 5000
