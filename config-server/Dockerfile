FROM maven:3.5.2-jdk-8-alpine AS MAVEN_BUILD

MAINTAINER Brian Hannaway

FROM openjdk:8-jre-alpine

WORKDIR /app

COPY /target/config-server-0.0.1-SNAPSHOT.jar /app/

ENTRYPOINT ["java", "-jar", "config-server-0.0.1-SNAPSHOT.jar"]