FROM openjdk:8
MAINTAINER tar@semafor.ch
# working directory for tomcat
VOLUME /tmp
#
ADD  timesystem-server.jar app.jar
# create user and set modification date
RUN useradd -r tomcat && sh -c 'touch /app.jar' && chown tomcat /app.jar
USER tomcat
# reduce tomcat startup 
ENTRYPOINT ["java", \
  "-Djava.security.egd=file:/dev/./urandom", \
  "-jar","/app.jar"]
