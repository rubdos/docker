FROM ubuntu:20.04

RUN apt-get update && \
    apt-get install -y jekyll ruby ruby-bundler gem \
                   make gcc ruby-dev autoconf build-essential \
                   openssh-client git wget curl&& \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
