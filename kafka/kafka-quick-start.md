---
description: Apache Kafka 3.4 기반 설치 및 사용 관련 문서
---

# Kafka Quick Start

## Kafka 다운로드 <a href="#kafkaquickstart-kafka" id="kafkaquickstart-kafka"></a>

[Download](https://www.apache.org/dyn/closer.cgi?path=/kafka/3.4.0/kafka\_2.13-3.4.0.tgz) 링크를 눌러 파일을 다운한다.

```bash
tar -xzf kafka_2.13-3.4.0.tgzcd kafka_2.13-3.4.0
cd kafka_2.13-3.4.0
```

## Kafka Environment 시작

Apache Kafka는 ZooKeeper나 KRaft를 사용해 시작할 수 있다.

### ZooKeeper 사용

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

### KRaft 사용

```bash
KAFKA_CLUSTER_ID="$(bin/kafka-storage.sh random-uuid)"
bin/kafka-storage/sh format -t $KAFKA_CLUSTER_ID -c config/kraft/server.properties
bin/kafka-server-start.sh config/kraft/server.properties
```

## Topic 생성

```bash
bin/kafka-topics.sh --create --topic testing --bootstrap-server localhost:9092
bin/kafka-topics.sh --describe --topic testing --bootstrap-server localhost:9092
```

## Topic에 Event 생성

```bash
bin/kafka-console-producer.sh --topic testing --bootstrap-server localhost:9092
```

## Event 읽기

```bash
bin/kafka-console-consumer.sh --topic testing --from-beginning --bootstrap-server localhost:9092
```
