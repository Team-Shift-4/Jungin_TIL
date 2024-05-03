---
description: Debezium에 관한 문서이다.
---

# Debezium

## What is Debezium

Debezium은 데이터베이스의 변경 사항을 캡처하여 애플리케이션이 이러한 변경 사항을 확인하고 이에 응답할 수 있도록 하는 분산 서비스 세트이다.

Debezium은 변경 이벤트 스트림의 각 데이터베이스 테이블 내의 모든 행 수준 변경 사항을 기록하고, 애플리케이션은 이러한 스트림을 읽어 변경 이벤트가 발생한 순서와 동일하게 확인한다.

## Debezium Architecture&#x20;

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Debezium Architecture</p></figcaption></figure>

### Debezium Server

Debezium Server는 Source Database에서 다양한 Messaging Infrastructure로 Change Event를 Steaming하는 구성이 가능하고 즉시 사용 가능한 Application이다.

아래는 Debezium Server를 사용하는 CDC Pipeline의 Architecture이다.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Debezium Server</p></figcaption></figure>

Debezium Server는 Debezium Source Connector 중 하나를 사용해 Source DB의 Change Event를 Capture하도록 구성된다.

Change Event는 JSON / Apache Avro와 같은 형식으로 Serialization 할 수 있다.

### Debezium Engine

Debezium Engine을 사용하는 경우 Kafka Connect를 통해 실행되지 않고 사용자 정의 Java Application에 내장된 Library로 실행된다.

전체 Kafka, Kafka Connect Cluster를 배포할 필요 없이 Application 자체 내에서 Change Event를 사용하거나 대체 Messaging Broker로 Change Event를 Streaming할 수 있다.
