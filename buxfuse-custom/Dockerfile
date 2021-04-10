FROM openjdk:11-jdk
RUN apt-get update
RUN apt-get install maven -y
RUN apt-get install git -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
COPY ./ /app_volume
WORKDIR /app_volume
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml
VOLUME /app_volume