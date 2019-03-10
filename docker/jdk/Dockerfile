FROM openjdk:8u191-jdk-alpine3.8

LABEL maintainer="yuanbin2014@gmail.com"

WORKDIR /root

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories && \
    apk update && \
    apk add --no-cache tzdata bash

ENV TZ=Asia/Shanghai \
    JAVA_RAM="-XX:InitialRAMPercentage=60.0 -XX:MaxRAMPercentage=95.0"

ENTRYPOINT java ${JAVA_RAM} "-XshowSettings:vm" "-version"
