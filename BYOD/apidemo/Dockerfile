FROM --platform=linux/amd64 eclipse-temurin:17-jdk-alpine

RUN addgroup -S --gid 12000 spring && adduser -S --uid 12000 spring -G spring

USER spring

ARG JAR_FILE=build/libs/apidemo-0.0.1-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
HEALTHCHECK CMD curl --fail http://localhost:3000 || exit 1