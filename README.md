# Kafka-docker-compose
Docker compose file for starting a Kafka and a Zookeeper cluster.

## Preconditions
You have to install Docker as well as Docker-compose (which is already included in most cases).

## How to run
Executed

    docker-compose up

## How to stop
Executed

    docker-compose down

## How to configure your application to interact with Kafka
### Application outside the Docker network
You have to configure the following:
Set one or all of the following as bootstrap-servers: localhost:9092,localhost:9093,localhost:9094
In case you plan to work with Avro, set the following as schema-registry: localhost:8081

### Application inside the Docker network
You have to configure the following:
Set one or all of the following as bootstrap-servers: kafka-1:19092,kafka-2:19093,kafka-3:19094
In case you plan to work with Avro, set the following as schema-registry: http://schema-registry:8081
