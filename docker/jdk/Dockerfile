FROM openjdk:8u191-jdk-alpine3.8

LABEL maintainer="yuanbin2014@gmail.com"

WORKDIR /root

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories && \
    apk update && \
    apk add --no-cache tzdata bash tini curl busybox-extras && \
    curl -L https://alibaba.github.io/arthas/install.sh | sh && \
    mv as.sh /usr/bin/as.sh

ENV TZ Asia/Shanghai

ENTRYPOINT ["/sbin/tini", "--"]

CMD ["java", "-XX:InitialRAMPercentage=40.0", "-XX:MaxRAMPercentage=70.0", "-XshowSettings:vm", "-version"]
