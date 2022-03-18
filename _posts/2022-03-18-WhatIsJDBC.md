---
title: What is JDBC - JDBC에 관하여
date: 2022-03-18 04:45:00 +09:00
categories: [Language, Java]
tags: [what_is]     # TAG names should always be lowercase
---

## Java Database Connectivity

JDBC 는 DataBase 연결과 작업을 위한 Java 표준 인터페이스로, 

Java 프로그램이 DB와 연결되어 Data 를 주고 받을 수 있게 해주는 Programming Interface 입니다.

## Function

쉽게 말하면 통역자의 역할을 합니다. JDBC API 가 없던 때는 DB 의 종류마다 

각각의 SQL 문 을 사용했어야 했습니다. 때문에, DB 의 종류에 따라 SQL 문의 작성 방법의 차이가 커

구현이 불편했습니다. 그래서 메서드나 전역변수 등을 통합하는 문법으로 통합한 것이 JDBC 입니다. 

### 응용프로그램과 DBMS 간의 통신을 번역

![Screen Shot 2022-03-18 at 3.40.41 PM.png](/Post_img/Language/Java/Screen_Shot_2022-03-18_at_3.40.41_PM.png)

## Java.sql.package

위 기능의 수행을 위해 Java 에서 제공하는 Interface 입니다.

### JDBC Driver manager

JDBC 아키텍처 중핵을 이룬 모듈에서 Java 의 프로그램과 JDBC 드라이버의 접속을 공급하는 기능을 수행.

### JDBC Driver API

JDBC 드라이버 매니저와 각 DBMS 의 벤더에서 제공하는 JDBC 드라이버가 서로 접속하기 위한 Interface.

### JDBC Driver

JDBC Driver 와 DBMS 접속을 제어하는 모듈로, 통상적으로 JDBC 드라이버는 각각 DBMS 벤더에서 제공하는

DBMS 에 ‘어떤 형태로 접속하는가’ 에 의해 크게 네가지 종류로 나눌 수 있으며, JDBC 에서 JAVA 프로그램에

사용하는 JDBC 드라이버 매니저와 DBMS 에 의존하는 JDBC 드라이버를 분리하는 것에서 

DBMS 벤더에 의존하지 않는 환경을 제공.