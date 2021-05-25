FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /builder
COPY . .
RUN mvn dependency:resolve  &&\
    mvn package

FROM openjdk:8-jre-alpine
COPY --from=builder /builder/target/worker-jar-with-dependencies.jar /builder/worker-jar-with-dependencies.jar
CMD [ "java", "-jar", "/builder/worker-jar-with-dependencies.jar" ]