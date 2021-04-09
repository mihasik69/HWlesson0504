FROM alpine/git as clone
VOLUME /app_volume
WORKDIR /app_volume
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git

FROM maven:3.6.0-jdk-11
WORKDIR /app_volume
RUN ls /app_volume
RUN mvn package -f "boxfuse-sample-java-war-hello/pom.xml"