# MAINTAINER        appleshan <apple.shan@gmail.com>
# DOCKER-VERSION    18.02.0-ce
#
# Dockerfile for learn python3
#

# Pull base image.
FROM alpine:latest

MAINTAINER appleshan <apple.shan@gmail.com>

# Install Python.
RUN set -xe \
    && apk add -U curl python3 \
    && curl -sSL https://bootstrap.pypa.io/get-pip.py | python3 \
    && rm -rf /var/cache/apk/*

WORKDIR /usr/src/myapp

# 使用阿里云的pip镜像
COPY pip.conf /root/.pip/pip.conf
COPY requirements.txt /usr/src/myapp/requirements.txt
RUN pip install -r /usr/src/myapp/requirements.txt

EXPOSE 8000

# Define default command.
CMD ["bash"]

# 构建镜像：
#
# docker build -t appleshan/python3-learn:0.1 .
#
# 拉起开发环境
# docker run -it --rm -v $(pwd)/myapp:/usr/src/myapp -w /usr/src/myapp appleshan/python3-learn:0.1 python helloworld.py
#
# 命令说明：
# -v $PWD/myapp:/usr/src/myapp : 将主机中当前目录下的 myapp 挂载到容器的 /usr/src/myapp
# -w /usr/src/myapp : 指定容器的 /usr/src/myapp 目录为工作目录
# python helloworld.py : 使用容器的 python 命令来执行工作目录中的 helloworld.py 文件
#
# 输出结果：
# Hello, World!
