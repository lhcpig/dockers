FROM centos:latest
MAINTAINER lhcpig <lhcpig@qq.com>

RUN yum install -y git
RUN git clone https://github.com/letsencrypt/letsencrypt .
RUN ./letsencrypt-auto --help
