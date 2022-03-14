---
title: Dev_Setting A
date: 2022-03-14 03:58:00 +09:00
categories: [MacOS, Dev_Setting]
tags: [Setting]     # TAG names should always be lowercase
---

---

환경

MacBook Pro(Intel Core)

Monterey OS(Version 12.2.1)

---

이번에 GitHub 와 Pages 를 초기화 하면서, MacBook 도 함께 포맷을 진행했습니다. 

이 기회에 앞으로 몇가지 작성자의 ‘Dev-setting style’ 을 하나씩 공유할 계획입니다.

## Dock

![Screen Shot 2022-03-14 at 10.56.15 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_10.56.15_AM.png)

Mac 을 처음 샀거나, 초기화를 했을때 볼 수 있는 화면입니다. WindowOS 와 다르게 IPhone, IPad 와 같이

아래 App 아이콘들이 있는 모습입니다. 이 부분을 Dock 이라고 합니다.

작성자는 저 중 절반은 실제로 사용하지 않고, 특히나 이 MacBook 은 온전한 Programming 용도기 때문에

필요한 부분을 제외하고 모두 삭제한 채 사용합니다. App 을 여는데는 Spotlight 를 대부분 사용하기 때문입니다.

![Screen Shot 2022-03-14 at 10.56.48 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_10.56.48_AM.png)

 

Dock 의 App 을 우클릭하고, Options > Remove from Dock 을 선택하면 App 을 정리할 수 있습니다.

![Screen Shot 2022-03-14 at 10.58.42 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_10.58.42_AM.png)

저는 주로 사용하는 Finder, Launchpad, Safari, Notes, Setting 만 두고 모두 정리했습니다.

만약 Dock 에 App 을 추가하고 싶다면, Finder > Applications 에서 Dock 으로 Drag&Drop 하면 됩니다.

## Finder

![Screen Shot 2022-03-14 at 11.00.26 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_11.00.26_AM.png)

Finder 의 초기 모습입니다. 사용하는데 별 문제는 없지만 조금만 편리하게 만들어 보겠습니다.

### Bar

![Screen Shot 2022-03-14 at 11.02.35 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_11.02.35_AM.png)

![Screen Shot 2022-03-14 at 11.03.01 AM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_11.03.01_AM.png)

View 탭을 클릭하면 Bar 설정을 할 수 있습니다. 저는 Tab Bar, Path Bar 를 주로 사용합니다.

## Side Bar

MacOS 는 사용자가 함부로 폴더나 파일을 변경할 수 없도록 프로그램 상 중요한 폴더나 파일을 숨겨두었습니다.

일반 사용자라면 불편함이 없겠지만, 개발자는 Path 설정과 같은 작업을 할 때 불편합니다.

때문에, 작성자는 아래와 같이 Hard Disk 등의 설정을 변경합니다.

![Screen Shot 2022-03-14 at 12.05.00 PM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_12.05.00_PM.png)

Finder > Preferences 에서 설정이 가능합니다. 

![Screen Shot 2022-03-14 at 5.07.59 PM.png](/Post_img/MacOS/Dev-Setting A/Screen_Shot_2022-03-14_at_5.07.59_PM.png)

## Hidden Folder

Sidebar Setting 으로 Disk 는 볼 수 있게 되었지만 사실 아직 폴더와 파일들이 숨겨져 있는 상태입니다.

주로 Terminal 로 접근할 수 있고, 편하기 때문에 굳이 사용하지는 않지만 가끔 필요할 경우가 생깁니다.

Termnal 에 아래의 명령을 입력하면 숨겨진 폴더를 확인할 수 있습니다.

 

```
defaults write com.apple.finder AppleShowAllFiles YES
```

이후 option 을 누른 채, Finder 를 우클릭하여 Relaunch 를 클릭합니다

![Screen Shot 2022-03-14 at 5.13.02 PM.png](/Post_img/MacOS/Dev-Setting%20A/Screen_Shot_2022-03-14_at_5.13.02_PM.png)

만약 다시 숨기고 싶다면, Termianl 에 아래 명령을 입력합니다.

```
defaults write com.apple.finder AppleShowAllFiles NO
```

이후 Relaunch 하면, 다시 숨길 수 있습니다.