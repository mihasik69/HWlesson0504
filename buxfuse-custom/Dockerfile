FROM alpine/git as clone
WORKDIR /app
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git

FROM maven:3.6.0-jdk-11
WORKDIR /app
COPY --from=clone /app/boxfuse-sample-java-war-hello /app
RUN mvn -f "pom.xml" clean package