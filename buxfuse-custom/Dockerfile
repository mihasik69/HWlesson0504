FROM alpine/git as clone
WORKDIR /app
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
COPY boxfuse-sample-java-war-hello /home/boxfuse-sample-java-war-hello

FROM maven:3.6.0-jdk-11-slim AS build
WORKDIR /home/boxfuse-sample-java-war-hello
RUN mvn -f "./pom.xml" clean package
COPY /target/hello-1.0.war /app
