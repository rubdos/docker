FROM java:8-jdk

MAINTAINER Ruben De Smet "ruben.de.smet@rubdos.be"
# Roughly based of https://github.com/appunite/docker/blob/master/android-java7-r24-4-1/Dockerfile

# Copyright [2015]
# 
#     Contributors:
#       * Jacek Marchwicki  <jacek.marchwicki@gmail.com>
#       * Karol Wojtaszek <karol@appunite.com>
# Copyright 2016 Ruben De Smet

RUN dpkg --add-architecture i386 && apt-get update && apt-get install -y --force-yes expect git wget libc6-i386 lib32stdc++6 lib32gcc1 lib32ncurses5 lib32z1 python curl

RUN cd /opt && wget --output-document=android-sdk.tgz --quiet http://dl.google.com/android/android-sdk_r24.4.1-linux.tgz && tar xzf android-sdk.tgz && rm -f android-sdk.tgz && chown -R root.root android-sdk-linux

# Setup environment
ENV ANDROID_HOME /opt/android-sdk-linux
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools

# Install sdk elements
RUN echo y | android update sdk --all --no-ui --filter "platform-tools,build-tools-23.0.2,build-tools-19.1.0,android-23,extra-android-support,extra-android-m2repository,sys-img-armeabi-v7a-android-21"

RUN which adb
RUN which android

# Create an Android Virtual Device
RUN echo "no" | android create avd --force -n test -t android-21 --abi armeabi-v7a

RUN apt-get clean
RUN mkdir -p /opt/workspace

WORKDIR /opt/workspace
