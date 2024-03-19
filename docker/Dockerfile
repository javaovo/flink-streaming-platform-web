FROM openjdk:11-jdk-slim

RUN  mkdir -p  /app

WORKDIR /app

ADD flink-streaming-platform-web.tar.gz /app
ADD flink.tar.gz /app

RUN chown -R root:root /app/flink-streaming-platform-web
RUN chown -R root:root /app/flink

ENV JAVA_OPTS ""

ENTRYPOINT java ${JAVA_OPTS} -jar /app/flink-streaming-platform-web/lib/flink-streaming-web-1.5.0.RELEASE.jar

