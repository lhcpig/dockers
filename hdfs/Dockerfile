FROM openjdk:latest
MAINTAINER lhcpig <lhcpig@qq.com>

ADD sources.list /etc/apt
RUN apt-get update && apt-get install -y openssh-server && apt-get clean
RUN ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa && \
  cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys && \
  chmod 0600 ~/.ssh/authorized_keys
RUN mkdir /var/run/sshd

RUN wget http://10.9.24.170/hadoop.tar.gz && \
  tar zxvf hadoop.tar.gz && \
  rm -rf hadoop.tar.gz
ENV HADOOP_HOME /hadoop-2.7.3
ENV HADOOP_CONF_DIR="${HADOOP_HOME}/etc/hadoop"
ENV HADOOP_LIBEXEC_DIR="${HADOOP_HOME}/libexec"
ENV PATH $PATH:${HADOOP_HOME}/sbin/:${HADOOP_HOME}/bin
RUN echo "export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64" >> ${HADOOP_HOME}/etc/hadoop/hadoop-env.sh
ADD hdfs-site.xml ${HADOOP_CONF_DIR}
ADD core-site.xml ${HADOOP_CONF_DIR}

RUN hdfs namenode -format
EXPOSE 50070 9000
#EXPOSE 50010 50020 50070 50075 50090 8020 9000
CMD ["/usr/sbin/sshd","-D"]
