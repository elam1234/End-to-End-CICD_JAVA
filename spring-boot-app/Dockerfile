FROM ubuntu:latest

RUN  apt-get update && apt install openjdk-17-jre -y

WORKDIR opt/app

ARG artifact=spring-boot-app/target/spring-boot-web.jar

COPY ${artifact} app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
