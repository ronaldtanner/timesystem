FROM openjdk:11.0.8-jre-slim
LABEL maintainer=tar@semafor.ch
#
ADD  target/timesystem-client.jar app.jar
# 
ENTRYPOINT ["java","-jar","/app.jar"]
