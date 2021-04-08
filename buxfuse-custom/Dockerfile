FROM ubuntu:20.04
RUN apt-get update
RUN apt-get install default-jdk -y
RUN apt-get install git -y
RUN apt-get install maven -y
VOLUME /app_volume
WORKDIR /app_volume
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
COPY --from=clone /app_volume/boxfuse-sample-java-war-hello /app_volume
RUN mvn -f "pom.xml" package