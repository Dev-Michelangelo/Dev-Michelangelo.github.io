---
title: Install Oracle
date: 2022-03-16 04:24:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz   2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”
- Oracle DataBase21C(Main) Version 21.3.0.0.0

---

작성자는 그동안 Oracle 11gXE 를 사용했었는데, 11g 가 서비스가 종료되어 더이상 다운로드 받을 수 없어

이렇게 된 김에 가장 최신 버전인 21C 를 사용하였습니다.

💡Info of 21C : [https://docs.oracle.com/en/database/oracle/oracle-database/21/whats-new.html](https://docs.oracle.com/en/database/oracle/oracle-database/21/whats-new.html)  

## Download

![5.png](/Post_img/WindowOS/InstallOracle/5.png)

2022.02 기준 Oracle 웹페이지 내에 아직 별도의 Oracle21C 다운로드 페이지가 없습니다.  
21C 는 19C 다운로드 페이지 하단 섹션에서 환경에 맞춰 다운로드 하면 됩니다. 

![7.png](/Post_img/WindowOS/InstallOracle/7.png)

작성자의 경우는 Oracle Home 이 설치될 구역과 Oracle DB 를 별도로 분리해 사용합니다.

때문에, Oracle Home 으로 사용할 Oracle 폴더에 압축 해제 했습니다.

## Install

![11.png](/Post_img/WindowOS/InstallOracle/11.png)

setup 파일을 실행합니다. 데이터베이스 설치 옵션 중 ‘단일 인스턴스’ 옵션을 선택했습니다.

![12.png](/Post_img/WindowOS/InstallOracle/12.png)

시스템 클래스를 데스크톱으로 선택했습니다. 이 블로그를 보고 참고하시는 분들은 대부분 학습 목적일 테니

동일하게 선택하셔도 무방합니다.

![13.png](/Post_img/WindowOS/InstallOracle/13.png)

가상계정을 선택합니다.

![14.png](/Post_img/WindowOS/InstallOracle/14.png)

데이터베이스 파일 디렉토리를 이전에 만들어 둔 C:\OracleDB 로 선택했습니다. 전역 데이터 베이스 이름은

별도로 지정할 필요가 없고 비밀번호 규칙도 개인 컴퓨터 작업에서 복잡도를 올릴 이유가 없습니다.

⚠️  메모리부족 에러 

위 단계에서 필요조건 검사로 넘어가기 전, 메모리 부족 에러가 발생할 수 있습니다. 

이때, 다른 프로그램들이 실행 중인지 확인하고 Oracle setup 을 제외한 프로그램들을 종료한 후 

다시 진행하면 에러가 사라집니다. 

![16.png](/Post_img/WindowOS/InstallOracle/16.png)

필요 조건 검사 완료 후, ‘요약’ 파트에서 방금 설정한 내용들을 확인 할 수 있습니다. 

만약 편집하고 싶은 내용이 있다면 편집을 눌러 편집하면 됩니다. 이후 설치를 클릭해 진행합니다.

![18.png](/Post_img/WindowOS/InstallOracle/18.png)

이후 자동으로 설치가 진행됩니다. 시간이 약 15~20 분 정도 소요됐습니다. 설치가 완료되면 종료합니다.