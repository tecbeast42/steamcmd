FROM ubuntu:16.04

ENV DEBIAN_FRONTEND noninteractive

RUN cd ~
RUN apt-get update && apt-get install -y wget curl vim nano lib32gcc1 ca-certificates net-tools lib32stdc++6 lib32z1 lib32z1-dev

RUN mkdir -p /opt/steamcmd &&\
    cd /opt/steamcmd &&\
    curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz


WORKDIR /opt/steamcmd

RUN ./steamcmd.sh +login anonymous +force_install_dir ../7days  +app_update 294420 validate +quit

WORKDIR /opt/7days
