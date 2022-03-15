---
title: Install Apache Tomcat
date: 2022-03-15 07:53:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz   2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”
- STS4 Version: 4.13.1.RELEASE, Build Id: 202201311654
- Apache Tomcat Version 10.0.16

---

Server 연동에 Apache Tomcat 을 사용하려 합니다. 별다른 어려움은 없습니다.

## Download

![4.png](/Post_img/WindowOS/InstallApacheTomcat/4.png)

Tomcat 웹사이트([https://tomcat.apache.org](https://tomcat.apache.org/)) 의 `Which Versions?` 탭을 클릭해 Version 을 확인합니다.

작성자는 Java11 을 사용하기 때문에 10.1.M10(alpha) 도 사용이 가능하지만, Maven repository 에 컨텐츠가

얼마 없는걸 확인하고, 10.0 version 을 선택했습니다.

![7.png](/Post_img/WindowOS/InstallApacheTomcat/7.png)

Download 탭에서 Version 을 선택하고 압축파일을 다운로드 합니다. 이후 압축을 해제합니다.

## New Server

![10.png](/Post_img/WindowOS/InstallApacheTomcat/10.png)

STS4의 `View → Server` 탭에서 `No servers are~` 을 클릭, Tomcat Version 을 선택합니다.

![11.png](/Post_img/WindowOS/InstallApacheTomcat/11.png)

`Browse` 를 클릭 하고 Tomcat 디렉토리를 선택합니다.

![14.png](/Post_img/WindowOS/InstallApacheTomcat/14.png)

![15.png](/Post_img/WindowOS/InstallApacheTomcat/15.png)

`Installed JRE` 를 선택하고 STS4 에 자체 내장된 Open JDK 가 아닌 설치한 JDK 를 추가합니다. 

Add 를 클릭합니다.

![16.png](/Post_img/WindowOS/InstallApacheTomcat/16.png)

Standard VM 을 선택하고 Next 를 클릭합니다. 이후 아래와 같이 설치한 JDK 디렉토리를 추가합니다.

![19.png](/Post_img/WindowOS/InstallApacheTomcat/19.png)

혹시 제 블로그를 참고하실 분들을 위해 이전글에서 언급을 미리 했지만 이 당시 JDK17 을 사용 중 이었습니다.

Spring Legacy Project 를 사용하려면 17 Version 은 맞지 않습니다.

💡 참고 : [https://dev-michelangelo.github.io/posts/LegacyProjectOnSTS4B/](https://dev-michelangelo.github.io/posts/LegacyProjectOnSTS4B/)

![20.png](/Post_img/WindowOS/InstallApacheTomcat/20.png)

마지막으로, 추가한 JDK 를 선택하고 `Apply and Close` 를 클릭합니다.

### New Server B

보통 위 과정을 거치면 Server 가 생성이 되는데, 생성되지 않았습니다. 그래서 한번 더 시도합니다.

![22.png](/Post_img/WindowOS/InstallApacheTomcat/22.png)

Tomcat Version 선택 후 설치한 JDK 디렉토리 입력 후 아직 Project 생성 전이니, Finish 를 클릭합니다.

![23.png](/Post_img/WindowOS/InstallApacheTomcat/23.png)

성공적으로 생성된 모습입니다.
