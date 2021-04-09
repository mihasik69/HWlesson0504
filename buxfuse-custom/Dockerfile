FROM alpine/git as clone
WORKDIR /app
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git

FROM openjdk:11-jdk-slim
RUN apt-get update
RUN apt-get install maven -y
WORKDIR /app_volume
COPY --from=clone /app /app_volume
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml

VOLUME /app_volume