# syntax=docker/dockerfile:1

FROM openjdk:oraclelinux8

WORKDIR /app

#Copy from Host to Container
COPY .mvn/ .mvn
COPY mvnw pom.xml ./

RUN ./mvnw dependency:go-offline

COPY src ./src

#Run inside image
CMD ["./mvnw", "spring-boot:run"]


