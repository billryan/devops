FROM openjdk:8u201-jdk-alpine

LABEL maintainer="yuanbin2014@gmail.com"

WORKDIR /root

RUN apk update && \
    apk add --no-cache tzdata bash tini curl busybox-extras && \
    curl -L https://alibaba.github.io/arthas/install.sh | sh && \
    mv as.sh /usr/bin/as.sh

ENV TZ Asia/Shanghai

ENTRYPOINT ["/sbin/tini", "--"]

CMD ["java", "-XX:InitialRAMPercentage=40.0", "-XX:MaxRAMPercentage=70.0", "-XshowSettings:vm", "-version"]
