FROM openjdk:11-jdk
VOLUME my_volume
RUN apt-get update
RUN apt-get install maven -y
RUN apt-get install git -y
WORKDIR /app
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml