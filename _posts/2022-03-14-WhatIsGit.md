---
title: What is git - git에 관하여
date: 2022-03-14 04:30:00 +09:00
categories: [Git, git]
tags: [what_is]     # TAG names should always be lowercase
---
---

환경

- MacBook Pro(Intel Core)
- Monterey OS(Version 12.2.1)
- git version 2.32.0 (Apple Git-132)

---

## Version Control System(VSC)

긴 작업기간을 필요로 하는 작업을 Word, PPT 로 진행할 때, 저장하지 않은 상태에서 컴퓨터가 급작스럽게

종료 되더라도 Cloud 서비스를 통해 내용이 소실되는걸 지킬 수 있습니다.

혹은 게임에서의 Checkpoint 기능을 통해 저장된 시점으로의 이동도 가능합니다.

## What is VSC?

위의 기능들은 VSC(Version Control System) 의 기능과 유사한 기능입니다.

공학과 소프트웨어 개발에서 팀 단위로 개발중인 소스코드나 설계도등 디지털 문서를 관리하는데 사용됩니다.

VSC 의 버전관리(Version control), 소스관리(source control), 소스코드관리(source code management) 를 통해 동일한 정보에 관한 여러버전을 관리할 수 있고 팀 단위의 작업에서 서로간의 작업물 상태를 동일하게 유지시키는 기능이 있습니다. VSC 는 많은 종류가 있고 그 중 git 이 대표적입니다. 

![git.png](/Post_img/Git/What%20is%20git/git.png)

## git

git은 VCS 종류 중 리눅스 커널 개발자인 ‘리누스 토르발스’ 에 의해 개발되고 2005년에 출시된 ‘분산버전시스템’ 중 하나입니다. 개발당시 완벽한 분산환경에서 빠르고 단순하게 수천개의 동시 다발적인 브랜치 작업이 수행 가능하고, 리눅스 커널같은 대형 프로젝트의 버전관리를 가능하게 하고자 하는 니즈를 토대로 개발되었습니다.

### **Advantages of git**

- 전세계 단위의 보유유저 수
- git 소셜 사이트인 Github
- 보유 유저 수에서 나오는 엄청난 단위의 튜토리얼과 프로젝트

## S**tructure and Function of git**

git 은 크게 ‘mater’ 서버와 mater 저장소의 완전한 사본을 가지는, Client 저장소로 구정됩니다.

서버와 클라이언트 둘 다 완전한 저장소를 가지고 있어, 저장소를 하나의 프로젝트라고 볼 수 있습니다.

### **Function of git**

- 로컬 및 원격 저장소 생성
- 로컬 저장소에 파일 생성 및 추가
- 수정 내역 로컬 저장소에 제출
- 파일 수정내역 추적
- 원격 저장소에 제출된 수정 내역을 로컬 저장소에 적용
- master에 영향을 끼치지 않는 브랜치 생성
- 브랜치 사이의 병합
- 브랜치를 병합하는 도중의 충돌 감지

## **How to install git?**

MacOS는 Homebrew 혹은 XCode 설치 시 git이 함께 설치됩니다.

WindowOS     :

MacOS        : [https://dev-michelangelo.github.io/posts/Homebrew/](https://dev-michelangelo.github.io/posts/Homebrew/)

## git Setting

- git을 사용하려면 git 회원 가입이 필요합니다. 회원가입은 [https://github.com](https://github.com/) 에서 간단히 가능합니다.
- MacOS 는 Terminal WindowsOS 는 ‘Git Bash’ 를 실행해 아래 명령어를 차례로 입력합니다.

```
git config --global user.name  "UserName"
git config --global user.email "User email"
```

- 이후 아래 코드로 확인합니다.

```
git config --l
```

![Screen Shot 2022-03-03 at 1.21.21 AM.png](/Post_img/Git/What%20is%20git/Screen_Shot_2022-03-03_at_1.21.21_AM.png)