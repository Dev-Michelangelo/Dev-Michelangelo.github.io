---
title: Legacy Project on STS4 A - STS4 Legacy Project 생성
date: 2022-03-15 06:24:00 +09:00
categories: [WindowOS, WebDev-Setting]
tags: [setting]     # TAG names should always be lowercase
---

---

환경

- 11th Gen Intel(R) Core(TM) i5-1135G7 @ 2.40GHz   2.40 GHz, RAM: 8.00GB, 64bit, x64
- WindowsOS 11
- JAVA_VERSION="11.0.13”
- STS4 Version: 4.13.1.RELEASE, Build Id: 202201311654

---

## Where is Spring Legacy Project on STS4?

![0.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/0.png)

STS4 는 Spring Legacy project 를 지원하지 않습니다. 작성자는 오랫동안 eclipse photon ver 을

사용했기 때문에, 초반에 번거로움이 있었습니다.

## STS3 Add-on for STS4

STS3 를 사용하면 간단히 해결할 문제지만, 구버전을 사용하고 싶진 않아 방법을 찾았습니다.

![2.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/2.png)

`Help → Eclipse Marketplace` 로 이동, STS 를 검색하고, `Spring tools 3 Add-on` 을 Install 합니다.

![3.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/3.png)

전체 체크한 후 Confirm 합니다.

![4.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/4.png)

accept 후 Restart 합니다.

![6.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/6.png)

Dashboard 가 나타나면 성공입니다.

## Where is Data Source Explorer, SQL file on STS4?

초기 설정을 해주고자 Perspactive 를 확인하자 몇가지가 없는게 눈에 보이고, 

`Show View → Data Source Explorer` `WEB -> SQL,CSS,XML file` 들이 표시되지 않습니다.

Stack Overflow 를 한참 뒤졌는데도 나오지 않아 여러가지 실험한 끝에 아래와 같이 해결했습니다.

### Help → Install New Software

![13.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/13.png)

`Work with:` 을 보면 [`https://download.eclipse.org/realeses/lastest`](https://download.eclipse.org/realeses/lastest) 가 있습니다. 버전 업을 위한 

링크일까 싶어, 원래 사용하던 Photon 을 lastest 부분에 입력해 검색하니 원하던 결과를 얻을 수 있었습니다.

![14.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/14.png)

![15.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/15.png)

필요한 Tools 은 Database Development, Web, Xml ~ 이기 때문에, 작성자는 두가지만 체크했습니다.

Market Place 와 설치방법은 동일합니다. `Next → accept` 합니다.

![20.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/20.png)

중간에 위와 같은 창이 나오는데, `Trust Seleted` 를 클릭하고 Restart 합니다.

![22.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/22.png)

Data Source Explorer 가 Show view 에 생성되었고, 나머지도 원하는 결과를 얻었습니다.

## UTF-8 Setting

한글이 깨지면 곤란하기에, UTF-8 세팅을 해줍니다.

### CSS

![27.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/27.png)

`Preferences → Web → CSS file` 로 접근해 `Encoding:` 을 UTF-8 으로 적용합니다. 이하 동일합니다.

![29.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/29.png)

`Web → HTML files`

![30.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/30.png)

`Web → JSP files`

![31.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/31.png)

`XML → XML files`

![33.png](/Post_img/WindowOS/LegacyProjectOnSTS4A/33.png)

마지막으로 Workspace 도 동일하게 설정합니다.