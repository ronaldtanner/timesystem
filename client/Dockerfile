FROM openjdk:8-jre
LABEL maintainer=tar@semafor.ch
#
ADD  target/timesystem-client.jar app.jar
# create user and set modification date
RUN useradd -r default && sh -c 'touch /app.jar'
# 
ENTRYPOINT ["java","-jar","/app.jar"]
