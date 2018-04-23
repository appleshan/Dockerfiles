FROM alpine:latest
MAINTAINER AppleShan <apple.shan@gmail.com>

# Define working directory.
WORKDIR /app
VOLUME /app

# Add MySQL configuration
COPY config/ /etc/mysql/conf.d/

RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*

# Expose ports.
EXPOSE 3306

# Define default command.
CMD ["/app/run.sh"]
