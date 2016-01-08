FROM ubuntu:latest
MAINTAINER lhcpig <lhcpig@qq.com>

WORKDIR /
RUN apt-get install -y unzip wget & apt-get clean & rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN wget https://github.com/letsencrypt/letsencrypt/archive/master.zip & unzip master.zip & rm -f master.zip

WORKDIR /letsencrypt-master
RUN ./letsencrypt-auto -v
