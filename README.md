# Timesystem
Simple demo project with java, spring-boot, maven and docker

* timesystem-server: a servlet based application which returns date, time and ip adresses of server and client on get requests.

* timesystem-client: sends periodically requests to the timeserver and prints the repsonses on stdout.

Both docker images are build by running the command in the project root directory:

  $ mvn package


Create the tmp directory with permissions to everyone: 

  mkdir -m=777 tmp

Start the timesystem either with
 
 docker-compose up -d
 
or
 
 docker-compose stack deploy -c docker-compose.yml timesystem
 
and view the differences.
