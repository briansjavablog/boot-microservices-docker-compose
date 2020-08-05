#FROM maven:3.5.2-jdk-8-alpine AS MAVEN_BUILD

#MAINTAINER Brian Hannaway

FROM openjdk:8-jre-alpine

WORKDIR /app

## Add wait script to the image - script pulled from https://github.com/ufoscout/docker-compose-wait/releases/download/2.7.3/wait /wait
COPY /scripts/wait /app/
RUN chmod +x /app

RUN apk --no-cache add curl

COPY /target/bank-account-service-0.0.1-SNAPSHOT.jar /app/

## ENTRYPOINT ["java", "-jar", "bank-account-service-0.0.1-SNAPSHOT.jar"]
CMD ./wait && java -jar bank-account-service-0.0.1-SNAPSHOT.jar
#CMD java -jar bank-account-service-0.0.1-SNAPSHOT.jar