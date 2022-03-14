---
title: Install JDK
date: 2022-03-14 11:51:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz   2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”

---

💡 본 글에 첨부된 이미지는 Java17 이나, 작성자는 Spring Legacy 를 위해 이후 Java11 으로 교체 했습니다.

만약, Spring Legacy 를 위해 설치한다면, Java 11 설치를 권장합니다. 설치와 설정과정은 11 과 17 동일합니다.

## Make Directory

![0.png](/Post_img/WindowOS/Install%20JDK/0.png)

C:\ 에 Resource 폴더를 생성합니다. 기호에 따라 다를 수 있지만, 작성자의 경우는 설치파일을 일정기간 보관합니다. 만약 문제가 발생하면 프로그램을 지우는 경우가 생기는데 다시 다운로드 하기 번거롭기 때문입니다.

## Install JDK

![4.png](/Post_img/WindowOS/Install%20JDK/4.png)

Google 혹은 Oracle 페이지에서 Java 11 을 검색해 Download 페이지로 이동합니다.

![5.png](/Post_img/WindowOS/Install%20JDK/5.png)

본인의 환경에 맞는 JDK 를 다운로드 합니다.

![9.png](/Post_img/WindowOS/Install%20JDK/9.png)

설치파일을 실행하고 설치 디렉토리를 설정합니다. 따로 지정하지 않아도 무방하나 작성자는 Pathname 이 

길어지는걸  불호하기 때문에, C:\ 바로 하위에 설치했습니다.이후 이전 버전과 다르게 간단히 설치됩니다.

## **Setting Java Path**

![2.png](/Post_img/WindowOS/Install%20JDK/2.png)

`Windows+R` ’sysdm.cpl’ 검색으로 `시스템 속성/고급` -> 환경변수로 진입합니다.

![4.png](/Post_img/WindowOS/Install%20JDK/4%201.png)

시스템변수의 `새로만들기` 를 클릭하고 변수이름을 지정, 변수 값에 JDK 가 설치된 디렉토리를 입력합니다.

![6.png](/Post_img/WindowOS/Install%20JDK/6.png)

확인을 클릭해 저장한 후 path 를 선택한 후 `편집` 을 클릭합니다.

![10.png](/Post_img/WindowOS/Install%20JDK/10.png)

환경변수 편집창 우측에 `새로만들기` 를 클릭한 후 `%<시스템 변수명>%\bin` 을 추가합니다.

이후 ‘위로  이동’ 을 사용해 맨 위로 올려줍니다. 사실 위로 이동은 하지 않아도 되는데 작성자가 알기로, 

쉽게 컴파일 에러를 방지하는 목적이라고 알고 있습니다. 

## Check

![13.png](/Post_img/WindowOS/Install%20JDK/13.png)

CMD 에 `javac -version` `java -version` 을 입력해 설치를 확인합니다. 

`path` 를 입력해 Path 가 정상적으로 설정 됐는지 확인합니다.

⚠️ 'javac은(는) 내부 또는 외부 명령, 실행 할 수 있는 프로그램, 또는 배치 파일이 아닙니다' 
응답 시, 환경변수 설정을 다시 확인합니다.