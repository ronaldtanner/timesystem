FROM openjdk:11.0.8-jre-slim
LABEL maintainer=tar@semafor.ch
#
ADD target/timesystem-server.jar app.jar
# create user and set modification date
RUN groupadd -r tomcat && useradd -r -g tomcat tomcat && \
  sh -c 'touch /app.jar' && chown tomcat:tomcat /app.jar
USER tomcat
# working directory for tomcat
VOLUME /tmp
ENTRYPOINT ["java", "-jar", "/app.jar"]
