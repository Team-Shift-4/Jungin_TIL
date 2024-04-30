---
description: Ark for CDC의 Ark Connector에 관한 문서이다.
---

# ACO CheckList

## Ark Connector

Ark Connector는 Ark for CDC의 Extract로 추출한 Change Data를 Kafka로 전송하는 모듈에 가깝다.

## Ark Connector 요구사항

### 모든 변경사항 캡처

#### DML 추출

* [x] INSERT 추출
* [x] UPDATE 추출
* [x] DELETE 추출

#### DDL 추출

* [ ] TRUNCATE 추출
* [ ] CREATE TABLE 추출
* [ ] DROP TABLE 추출
* [ ] ALTER TABLE 추출

#### Tombstone Event 처리

* [ ] Tombstone Event 처리 -> 기능은 만들었으나 정상 동작하지 않음

### 추가 메타데이터 캡처

#### 필요해 보이는 Template

* [ ] SCHEMA\_OBJECT
* [ ] CATALOG
* [ ] SCHEMA
* [ ] OBJECT
* [ ] POSITION
* [ ] CURRENT\_TIMESTAMP\[]
* [ ] CURRENT\_DATE\[]
* [ ] CURRENT\_TIME\[]
* [ ] TO\_UPPER\[]
* [ ] TO\_LOWER\[]
* [ ] SCN
* [ ] OP\_TYPE
* [ ] PK
* [ ] STATIC\_MAP
* [ ] NULL
* [ ] COL\_VALUE
* [ ] GROUP\_NAME ->  추출 대상 설정 Alias

#### OGG for Bigdata가 보유하고 있는 Template

* [ ] ${fullyQualifiedTableName} -> SCHEMA\_OBJECT
* [ ] ${catalogName} -> CATALOG
* [ ] ${schemaName} -> SCHEMA
* [ ] ${tableName} -> OBJECT
* [ ] ${opType} -> OP\_TYPE
* [ ] ${primaryKeys} -> PK
* [ ] ${position} -> POSITION
* [ ] ${opTimestamp}
* [ ] ${emptyString}
* [ ] ${staticMap\[]} -> STATIC\_MAP\[]
* [ ] ${columnValue\[]} -> COL\_VALUE\[]
* [ ] ${currentTimestamp\[]} -> CURRENT\_TIMESTAMP
* [ ] ${null} -> NULL
* [ ] ${custom\[]}
* [ ] ${operationCount}
* [ ] ${insertCount}
* [ ] ${updateCount}
* [ ] ${deleteCount}
* [ ] ${truncateCount}

### Filter 기능

* [x] 추출 테이블 필터
* [ ] 추출 제외 테이블 필터 -> 정상 동작하지 않음\[AFC Post Mapper]
* [ ] 추출 컬럼 필터 -> 정상 동작하지 않음\[AFC Post Mapper]
* [ ] 추출 제외 컬럼 필터 -> 정상 동작하지 않음\[AFC Post Mapper]
* [ ] 특정 Operation 필터 -> 정상 동작하지 않음\[AFC Post Config]

### Masking 기능

* [ ] 특정 컬럼 마스킹

### Topic 명 변경

* [ ] 고정 명 변경
* [ ] Template 사용 변경
* [ ] 둘 다 가능

### Column 명 변경

* [ ] 컬럼 명 변경\[AFC Mapper]

### Column Data 변경

* [ ] 긴 Char Data 추출 시 절삭

#### Column 형 변환

* [ ] Byte to Char
* [ ] Byte to BASE64
* [ ] Byte to Hex
* [ ] Byte to Unicode
* [ ] Number to Char
* [ ] Date to Char
* [ ] Char to Date
* [ ] All to Char

### Message Format 변경

* [x] JSON
* [x] JSON\_V1
* [x] CONNECT\_JSON
* [x] CONNECT\_AVRO
* [ ] Class 형식으로 확장

### Message 보안

* [ ] 전송 암호화\[Kerberos]
* [ ] Message 암호화

