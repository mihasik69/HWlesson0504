FROM alpine/git as clone
WORKDIR /app
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git

FROM maven:3.6.0-jdk-11-slim
WORKDIR /app_volume
COPY --from=clone /app /app_volume
RUN mvn package -f boxfuse-sample-java-war-hello/pom.xml
CMD cp -r /app_volume/boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps/hello-1.0.war

VOLUME /app_volume