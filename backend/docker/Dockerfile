FROM ubuntu:18.04

RUN apt-get update -y && \
apt-get install default-jre -y

ARG jarName
ARG profile
ARG serverPort

COPY . app/
WORKDIR app

ENV JAR_NAME $jarName
ENV PROFILE $profile

ENTRYPOINT java -jar $JAR_NAME \
--spring.profiles.active=$PROFILE

EXPOSE $serverPort