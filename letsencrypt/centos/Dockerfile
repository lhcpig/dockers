FROM centos:latest
MAINTAINER lhcpig <lhcpig@qq.com>

WORKDIR /
RUN yum install -y git
RUN git clone https://github.com/letsencrypt/letsencrypt

WORKDIR /letsencrypt
RUN ./letsencrypt-auto --help
