FROM openjdk:8-jdk-alpine

RUN apk add --no-cache maven

COPY . /redact

WORKDIR /redact

RUN mvn clean install

RUN mv target/*.jar redact.jar

EXPOSE 2222

CMD ["/usr/bin/java", "-jar", "redact.jar", "--server.port=2222", "redact"]
