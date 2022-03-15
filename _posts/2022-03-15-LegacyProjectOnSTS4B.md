---
title: Legacy Project on STS4 B - java.lang.exceptionininitializererror
date: 2022-03-15 07:11:00 +09:00
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

## java.lang.exceptionininitializererror

![3.png](/Post_img/WindowOS/LegacyProjectOnSTS4B/3.png)

모든 준비가 다 끝나고, Legacy Project 를 생성하던 중 `java.lang.exceptionininitializererror` 가 

발생했습니다. 경험상 컴파일 에러인 듯 한데, 이것도 Stack Overflow 를 뒤져봐도 나오지 않았습니다.

구글링을 했을때 여러가지 방법이 나와있지만, 작성자는 아래 방법으로 해결했습니다.

## Check Java version

첫번째는 Java version 문제입니다. STS Official GitHub 에서 예전부터 Java17을 지원한다는 소식을 보고

최신버전인 Java17 을 설치했는데 Spring 자체는 17을 지원하지만, Legacy Project 는 지원하지 않아 생긴

문제였습니다. 때문에, Java11 으로 교체했습니다. 하지만 에러는 고쳐지지 않았습니다.

## Check ini file

Stack Overflow 를 보면, `ini file` 을 수정해 해결한 사례가 몇가지 있었습니다. 하지만 작성자의 경우 

적용되지 않았습니다. 여러 추론 끝에 아래의 방법으로 해결했습니다.

![6.png](/Post_img/WindowOS/LegacyProjectOnSTS4B/6.png)

```
-vm
plugins/org.eclipse.justj.openjdk.hotspot.jre.full.win32.x86_64_17.0.1.v20211116-1657/jre/bin
```

원본은 위와 같이 `-vm` 에 Open jdk 가 설정되어 있습니다. 아마 Open JDK 를 지원하지 않거나 

작성자와 Java version 이 맞지 않거나 둘 중 하나라 생각해, 기존의 내용을 지우고 

현재 설치한 Java11 의 path 를 작성해 구동했습니다. 

💡 이후 혹시 몰라 한번 더 Java17 버전으로 교체하고 path 를 재입력 한 뒤, Java version 을 17 으로 작성한 뒤 

구동해 보았으나 동일한 오류가 발생했습니다. 때문에, Java11 을 권장합니다.  

![11.png](/Post_img/WindowOS/LegacyProjectOnSTS4B/11.png)

정상적으로 Legacy Project 가 생성된 모습입니다. Programming 은 세팅이 반이라는 말이 너무 공감됩니다.