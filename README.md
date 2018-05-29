Projeto modelo para avaliação técnica de desenvolvedores spring - redspark
========
O projeto modelo tem a ideal de mostrar diversas práticas para ajudar o desenvolvedor na tomada de decisão.

## Required

### Docker
[Link to Installation Section](https://www.docker.com/)

#### Mac OSX
[Link to Installation Section on Mac](https://docs.docker.com/installation/mac/)

Run this once after install docker in your console to add the hostname "http://docker" to you hosts:

### boot2docker
```
IP=$(boot2docker ssh ip addr show eth1 |sed -nEe 's/^[ \t]*inet[ \t]*([0-9.]+)\/.*$/\1/p'); sudo bash -c "echo '' >> /etc/hosts; echo $IP docker >> /etc/hosts"

````
### docker-machine
```
IP=$(docker-machine ip default); sudo bash -c "echo '' >> /etc/hosts; echo $IP docker >> /etc/hosts"

```

# Build

## Requisits
Maven | [http://maven.apache.org/](http://maven.apache.org/)

JDK8 Oracle/Sun | [http://www.oracle.com/technetwork/java/javase/downloads/index.html](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

Lombok | [http://projectlombok.org/](http://projectlombok.org/)

Lombok install:
Run this:
```
java -jar ~/.m2/repository/org/projectlombok/lombok/1.16.2/lombok-1.16.2.jar
```
After run, it's necessary to specify your current Eclipse installation, attention to select de link 'eclipse' in Eclipse installation folder and click Install.

## Back-End build and run
mvn clean install -f server/pom && sudo docker-compose up

## Artifacts
server/target/spring-codetest.jar


