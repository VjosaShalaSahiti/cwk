FROM openjdk:8-jdk-alpine

RUN apk add --no-cache maven

COPY . /web

WORKDIR /web

RUN mvn clean install

RUN mv target/*.jar web.jar

EXPOSE 2222

CMD ["/usr/bin/java", "-jar", "web.jar", "--server.port=4444", "web"]
