---
title: What is Java ORM - Object Relational Mapping
date: 2022-03-19 03:22:00 +09:00
categories: [Language, Java]
tags: [what_is]     # TAG names should always be lowercase
---

## Impedance Mismatch(객체-관계 불일치)

RDB 는 많은 장점을 가지고 있지만, 완벽하지 않아 초창기에 불만이 많았습니다. 그 중 애플리케이션 개발자의

대표적인 불만은 관계형 모델과 메모리 내 구조간 차이, 객체-관계 불일치 입니다. 

관계형 데이터 모델은 테이블과 행으로 데이터 즉, 관계와 튜플로 데이터를 구조화 합니다.

관계형 모델에서 튜플은 이름-값의 집합이고, 관계는 튜플의 집합입니다. SQL 에서 모든 연산은 관계를 소비하고

반환하는데 이는 관계 대수로 설명합니다. 상술한 관계의 기반은 단순함을 제공하지만 제약이 생기게 되는데

특히 관계형 튜플 안의 값은 단순해야 하고, 중첩된 레코드나 리스트 등 다른 구조를 포함할 수 없습니다.

그 결과, 위와 같은 제약이 없어 상대적으로 관계보다 복잡한 구조를 사용할 수 있는 메모리 내 데이터 구조를

DB 에 저장하기 위해, 관계형 표현으로 변환이 필요하게 됩니다. 

![rdb-tables.png](/Post_img/Language/Java/What%20is%20JavaORM/rdb-tables.png)

1990 년대에는 RDB 가 메모리내 데이터 구조를 그대로 디스크에 저장하는 새로운 DB 로 대체 될 것이라 

생각 했습니다. 당시, OOP 가 성장 하고, ODB 가 등장 했었기 때문인데, 현재와서 살펴보면 OOP 와 달리

ODB 는 성장하지 못했습니다. RDB 가 통합 방법으로서의 역할 강조, 데이터 조작을 위한 표준언어(SQL) 지원

애플리케이션 개발자와 DB 관리자 직종 분리 심화 등의 요인에 힘을 입었기 때문입니다. 

**A. 세분성 (Granularity):** 경우에 따라 DB 내 테이블 수보다 더 많은 클래스를 가진 모델이 생길 수 있음.

(RDB 데이터 타입은 Vendor 마다 상이하며, 더 이상 정규화가 어렵습니다.)

**B. 상속성 (Inheritance):** RDBMS 는 Primary key 를 이용하여 동일성을 적용합니다. 

하지만 Java 는 객체 식별 (`a==b`) 과 객체 동일성(`a.equals(b)`) 을 모두 정의 합니다.

**C. 연관성 (Associations):** OOP 는 방향성 있는 객체의 참조(reference)를 사용해 

연관성을 나타내지만, RDBMS는 방향성이 없는 외래키(foreign key)를 이용해서 나타냅니다.

**D. 탐색 (Navigation):** Java 와 RDBMS 에서 객체를 접근하는 방법이 근본적으로 다릅니다. 

Java 는 그래프형태로 하나의 연결에서 다른 연결로 이동하며 탐색하지만, RDBMS 는 일반적으로 SQL 문을 

최소화하고 JOIN 을 통해 여러 엔티티를 로드하고 원하는 대상 엔티티를 선택하는 방식으로 탐색합니다.

## ORM(Object Relational Mapping)

ORM 은 객체의 관계를 바탕으로 SQL 문에 관해 자동적으로 생성 불일치를 해결합니다.

### P**ros and Cons**

**Pros**

A. 객체 지향적 코드로 인해, 보다 직관적이며, 비즈니스로직 에 집중할 수 있습니다.

B. 재사용, 유지보수의 편리성이 증가합니다.

C. DBMS 에 대한 종속성이 줄어듭니다.

**Cons**

A. ORM 으로만 서비스를 구현하기엔 한계가 있습니다.

B. 프로시저가 많은 시스템에선 ORM의 객체 지향적인 장점을 활용하기 어렵습니다.

매핑패턴을 구현한 iBATIS 나 Hibernate 와 같은 객체-관계 매핑 프레임워크가 널리 사용되면서

객체-관계 불일치 이슈는 완화 되었지만, 상술한 것과 같이 DB 나 쿼리 성능을 지나치게 무시하면 다른 문제가

발생할 수 있습니다.