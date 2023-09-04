FROM openjdk:8-jdk-alpine

RUN apk add --no-cache maven

COPY . /registration

WORKDIR /registration

RUN mvn clean install

RUN mv target/*.jar registration.jar

EXPOSE 8761

CMD ["/usr/bin/java", "-jar", "registration.jar", "--server.port=8761", "registration"]
