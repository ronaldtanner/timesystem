FROM openjdk:8
LABEL maintainer=tar@semafor.ch
#
ADD target/timesystem-server.jar app.jar
# create user and set modification date
RUN useradd -r tomcat && sh -c 'touch /app.jar' && chown tomcat /app.jar
USER tomcat
# working directory for tomcat
VOLUME /tmp
# reduce tomcat startup 
ENTRYPOINT ["java", \
  "-Djava.security.egd=file:/dev/./urandom", \
  "-jar","/app.jar"]
