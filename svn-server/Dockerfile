FROM ubuntu:14.04

MAINTAINER lhcpig

ADD sources.list /etc/apt/sources.list

RUN apt-get update && \
    apt-get install -y subversion && \
    svnadmin create /svn-bak && \
    chmod -R 777 /svn-bak && \
    apt-get clean && rm -fr /var/lib/apt/lists/* /tmp/* /var/tmp/*

ADD svnserve.conf /svn-bak/conf/svnserve.conf
ADD passwd /svn-bak/conf/passwd

EXPOSE 3690
CMD [ ! -e /svn/db ] && cp -r /svn-bak/* /svn/; svnserve -dr /svn; while pidof svnserve >/dev/null; do sleep 1; done
    



