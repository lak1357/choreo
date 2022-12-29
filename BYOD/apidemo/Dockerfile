FROM --platform=linux/amd64 eclipse-temurin:17-jdk-alpine
#FROM --platform=linux/amd64 openjdk:17-jdk-alpine
#RUN addgroup -S --gid 15011 spring && adduser -S --uid 15011 spring -G spring
RUN adduser -u 18877 spring
#RUN groupadd -r spring && useradd -r -g spring -u 10001 spring
USER spring
ARG JAR_FILE=build/libs/apidemo-0.0.1-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]