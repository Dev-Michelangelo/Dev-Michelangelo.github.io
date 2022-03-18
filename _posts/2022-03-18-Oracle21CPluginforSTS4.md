---
title: Oracle21C Connect for STS4 - OracleDB 연결하기(21C)
date: 2022-03-18 05:41:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz 2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”
- Oracle DataBase21C(Main) Version 21.3.0.0.0
- JDBC: OJdbc Driver 11

---

## Download OJDBC Driver

Oracle21 을 Java DB 로 사용하기 위해서는 OJDBC Driver 가 필요합니다.

JDBC 에 관하여: [https://dev-michelangelo.github.io/posts/WhatIsJDBC/](https://dev-michelangelo.github.io/posts/WhatIsJDBC/)

[https://www.oracle.com/kr/database/technologies/appdev/jdbc.html](https://www.oracle.com/kr/database/technologies/appdev/jdbc.html) 에서 다운로드 할 수 있습니다.

![6.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/6.png)

Oracle DB와 JDK 환경에 맞춰 다운로드 하면 됩니다. 작성자는 Oracle21C, JDK11 과 호환되는 

OJDBC11 을 사용합니다. Download 후 압축해제 합니다.

## New Connection

![2.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/2.png)

`Data Source Explorer → DataBase Connections → New` 로 이동 후 `Oracle Database` 를 선택합니다.

### New Driver Definition

![3.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/3.png)

`New Driver Definition` 아이콘을 클릭합니다.

![4.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/4.png)

`Name/Type` 탭에서 Oracle Driver Version 을 선택합니다. 저는 11을 선택했습니다.

![7.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/7.png)

`JAR List` 탭에서 OJDBC 14 를 삭제한 후 이전 과정에서 설치한 OJDBC 를 연결합니다. 항상 JAR List 에 14이

디폴트로 설정되어 있던데, 이유가 궁금하니 다음에 한번 찾아봐야겠습니다. `Properties` 를 확인하고 종료합니다.

![9.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/9.png)

`DataBase Instance` 를 `SID` 로 체크하고 전역 데이터 베이스명을 입력합니다. 

이후, `User Name` 과 `PW` 를 입력합니다.

![10.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/10.png)

Test Connection 결과를 확인합니다. 작성자는 MacOS 에서 이 과정 중 Ping Fail 을 겪은적이 많습니다.

덕분에 의도치 않게 에러를 많이 알게 되었는데, 이부분은 정리해서 나중에 업로드 하려고 합니다.

![13.png](/Post_img/WindowOS/Oracle21C%20Plugin%20for%20STS4%20/13.png)

성공적으로 연결된 모습입니다.