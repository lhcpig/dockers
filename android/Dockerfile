FROM java:8-jdk
MAINTAINER lhcpig <lhcpig@qq.com>

ENV ANDROID_SDK_VERSION r24.4.1
WORKDIR /opt
RUN curl -sLO https://dl.google.com/android/android-sdk_${ANDROID_SDK_VERSION}-linux.tgz && \
  tar zxvf android-sdk_${ANDROID_SDK_VERSION}-linux.tgz && \
  ln -s android-sdk_${ANDROID_SDK_VERSION}-linux android-sdk && \
  rm android-sdk_${ANDROID_SDK_VERSION}-linux.tgz

ENV ANDROID_HOME /opt/android-sdk
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools

ENV GRADLE_VERSION 2.2.1
WORKDIR /usr/bin
RUN curl -sLO https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-all.zip && \
  unzip gradle-${GRADLE_VERSION}-all.zip && \
  ln -s gradle-${GRADLE_VERSION} gradle && \
  rm gradle-${GRADLE_VERSION}-all.zip

ENV GRADLE_HOME /usr/bin/gradle
ENV PATH $PATH:$GRADLE_HOME/bin

RUN mkdir /app
WORKDIR /app
