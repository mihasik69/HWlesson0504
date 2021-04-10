FROM openjdk:11-jdk
RUN apt-get update
RUN apt-get install maven -y
RUN apt-get install git -y
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml
CMD cp -r ./boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps
VOLUME /app_volume
