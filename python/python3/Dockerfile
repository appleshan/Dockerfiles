#
# Dockerfile for python3
#

# Pull base image.
FROM alpine

MAINTAINER kev <noreply@easypi.info>

# Install Python.
RUN set -xe \
    && apk add -U curl python3 \
    && curl -sSL https://bootstrap.pypa.io/get-pip.py | python3 \
    && rm -rf /var/cache/apk/*

# Define default command.
CMD ["python3"]
