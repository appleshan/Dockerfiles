# Wine docker image base
FROM debian:jessie
MAINTAINER Jessie Frazelle <jess@linux.com>

# install wine
RUN apt-get update && apt-get install -y \
    wine \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

ENV HOME /root
WORKDIR $HOME
