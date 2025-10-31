FROM maven:3.8.4-openjdk-17 AS build

RUN groupadd -r mygroup && useradd -r -g mygroup -m -d /home/myuser myuser
USER myuser

ARG JAR_FILE=spring-boot-data-jpa-mysql/target/*.jar
COPY ${JAR_FILE} app.jar
EXPOSE  8080

ENTRYPOINT ["java","-jar","app.jar/"]