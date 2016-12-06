FROM openjdk:8-jre
MAINTAINER tar@semafor.ch
#
ENV TIMESERVER timeserver
#
WORKDIR /apphome
COPY  timesystem-client.jar app.jar
# set modification date
RUN sh -c 'touch app.jar'
# 
RUN groupadd -r timeclient && \
    useradd -r -g timeclient timeclient
USER timeclient
ENTRYPOINT ["java", "-jar","app.jar"]
