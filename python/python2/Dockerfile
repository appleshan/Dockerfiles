#
# Dockerfile for python2
#

# Pull base image.
FROM alpine

MAINTAINER kev <noreply@easypi.info>

# Install Python.
RUN set -xe \
    && apk add -U curl python \
    && curl -sSL https://bootstrap.pypa.io/get-pip.py | python \
    && rm -rf /var/cache/apk/*

# Define default command.
CMD ["python"]
