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

