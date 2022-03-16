---
title: Ora-65096 Invalid common user or role name
date: 2022-03-16 05:27:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz   2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”
- Oracle DataBase21C(Main) Version 21.3.0.0.0
- SQL*Plus: Release 19.0.0.0.0

---

‘Ora-65096 Invalid common user or role name’ 

혹은, ‘ORA-65096: 공통 사용자 또는 롤 이름이 부적합 합니다.’ 에러는 Oracle12C 이후 계정생성 시 c## 을

붙여줘야 생성이 가능하도록 변경되어 발생되는 오류 입니다. 

물론, 번거롭기 때문에 아래 쿼리문을 사용해 12C 이전 Version 처럼 작성이 가능합니다.

```
ALTER SESSION SET "_ORACLE_SCRIPT"=true;
```