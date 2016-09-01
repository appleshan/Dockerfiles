# Wine docker image base
FROM debian:jessie
MAINTAINER Jessie Frazelle <jess@linux.com>

# install wine
RUN dpkg --add-architecture i386 \
    && apt-get update \
    && apt-get install -y \
    wine32 \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

ENV HOME /root
WORKDIR $HOME
