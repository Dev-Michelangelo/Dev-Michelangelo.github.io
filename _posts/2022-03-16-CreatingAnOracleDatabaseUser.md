---
title: Creating an Oracle database user
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

Oracle DBMS를 위해, SQL Plus 를 사용합니다.

## SQL Plus

![0.png](/Post_img/WindowOS/CreatingAnOracleDatabaseUser/0.png)

CMD 에 `sqlplus` 를 입력해 SQL 을 실행합니다.

![1.png](/Post_img/WindowOS/CreatingAnOracleDatabaseUser/1.png)

권한 부여를 위해 관리자 계정 로그인 한 뒤, `conn/as sysdba` 명령을 통해 Oracle `sysdba` 에 접속합니다.

이후 아래 명령을 통해 계정을 생성합니다.

## Create Account

```
create user <ID> identified by <PW>;
```

만약, 생성 후에 PW 를 변경하고 싶다면, 아래 명령으로 변경합니다.

```
alter user <ID> identified by <PW>;
```

⚠️ ORA65096: Error

Oracle12c Version 이후 부터 계정 생성및 권한 부여 시, ID 값 앞에 c##을 붙여줘야 합니다.

번거롭다면 참고: [https://dev-michelangelo.github.io/posts/Ora65096InvalidCommonUserOrRoleName/](https://dev-michelangelo.github.io/posts/Ora65096InvalidCommonUserOrRoleName/)

## A**uthorization**

아래 명령을 통해 권한을 부여합니다.

```
grant connect, resource dba to <ID>;
```

이후, `commit` 명령으로  Commit 합니다.

## C**hange port**

Oracle 21C 의 경우 Port 충돌이 없어, 따로 변경하지 않았지만 11g 의 경우 Tomcat 과의 충돌이 있었습니다.

이는 Oracle 과 Tomcat 이 모두 Port8080 을 사용하기 때문인데, 기호에 따라 다르겠지만 

작성자는 Tomcat 의 Port 를 변경하기 보다 Oracle 의 Port 를 변경하는 편 입니다. 결과는 동일합니다.

아래 명령을 통해 현재 Port 를 확인합니다.

```
select dbms_xdb.gethttpport() from dual;
```

아래 명령으로 Port8080 을 Port9090 으로 교체합니다.

```
exec dbms_xdb.sethttpport(9090);
```