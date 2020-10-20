FROM openjdk:8

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/docker-hy/spring-example-project

EXPOSE 8080
WORKDIR /spring-example-project

RUN ./mvnw package
CMD java -jar ./target/docker-example-1.1.3.jar