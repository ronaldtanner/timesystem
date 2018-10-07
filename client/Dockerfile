FROM openjdk:8-jre
LABEL maintainer=tar@semafor.ch
#
ADD  target/timesystem-client.jar app.jar
# 
ENTRYPOINT ["java","-jar","/app.jar"]
