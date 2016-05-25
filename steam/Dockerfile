FROM ubuntu:16.04

ENV DEBIAN_FRONTEND noninteractive

RUN cd ~
RUN apt-get update && apt-get install -y wget curl vim nano lib32gcc1

RUN mkdir -p /opt/steamcmd &&\
    cd /opt/steamcmd &&\
    curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz


WORKDIR /opt/steamcmd

# This container will be executable
ENTRYPOINT ["./steamcmd.sh"]