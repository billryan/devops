FROM billryan/jdk:8

LABEL maintainer="yuanbin2014@gmail.com"

ENV SCALA_VERSION 2.12

ENV KAFKA_VERSION 2.2.1

RUN wget https://www-us.apache.org/dist/kafka/${KAFKA_VERSION}/kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz && \
    mkdir -p /opt && \
    tar xzvf kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz -C /opt && \
    rm kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz && \
    mv /opt/kafka_${SCALA_VERSION}-${KAFKA_VERSION} /opt/kafka

WORKDIR /opt/kafka

ENTRYPOINT ["bin/kafka-run-class.sh"]

CMD []

