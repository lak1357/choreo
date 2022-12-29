FROM --platform=linux/amd64 openjdk:17-jdk-alpine
RUN groupadd -r spring && useradd -r -g spring -u 10001 spring
USER spring:spring
ARG JAR_FILE=build/libs/apidemo-0.0.1-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]