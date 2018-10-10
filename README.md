# Docker-kafka-kit
This repository provides a convenient way to start kafka in docker for development and testing purposes.

## Run
```shell
git clone https://github.com/Gr1f0n6x/docker-kafka-kit.git ./docker-kafka-kit
cd ./docker-kafka-kit
docker-compose up
# or
docker-compose up -d # (for running it in detached mode)
```

It will start the following containers:
- zookeeper: `localhost:2181` (confluentinc/cp-zookeeper:5.0.0)
- kafka-broker: `localhost:29092` (confluentinc/cp-enterprise-kafka:5.0.0)
- schema-registry: `localhost:8081` (confluentinc/cp-schema-registry:5.0.0)
- kafka-connect: `localhost:8083` (confluentinc/cp-kafka-connect:5.0.0)
- kafka-rest-proxy: `localhost:8082` (confluentinc/cp-kafka-rest:5.0.0)
- kafka-topics-ui: `localhost:8001` (landoop/kafka-topics-ui:0.9.4)
- schema-registry-ui: `localhost:8000` (landoop/schema-registry-ui:0.9.5)

## Schema registry ui
Using schema registry ui you can easily create new schema and update existing schemas
![schema-registry-ui](/images/schema-registry-ui.png)
![schema-registry-new-schema-ui](/images/schema-registry-new-schema.png	)

## Kafka topics ui
Assuming that you have already installed kafka binaries, you can run this command:
```shell
kafka-topics --create --topic test --zookeeper localhost:2181 --replication-factor 1 --partitions 1
```
and, in result, you will see created topic in kafka topics ui web page:
![kafka-topics-ui](/images/kafka-topics-ui.png)
