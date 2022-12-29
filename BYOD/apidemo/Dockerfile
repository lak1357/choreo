FROM --platform=linux/amd64 eclipse-temurin:17-jdk-alpine
#FROM --platform=linux/amd64 openjdk:17-jdk-alpine
#RUN addgroup -S --gid 15011 spring && adduser -S --uid 15011 spring -G spring
#RUN adduser -S -u 18877 spring && addgroup -g 19877 spring && usermod -a -G spring spring
#RUN 
#RUN groupadd -r spring && useradd -r -g spring -u 10001 spring
ENV UID=9000
ENV GID=9000

RUN addgroup -S --gid 9000 spring && adduser -S --uid 9000 spring -G spring

USER spring

ARG JAR_FILE=build/libs/apidemo-0.0.1-SNAPSHOT.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
HEALTHCHECK CMD curl --fail http://localhost:3000 || exit 1