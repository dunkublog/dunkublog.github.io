---
layout: single
title: "깃허브 블로그 Minimal Mistakes 테마 프로필 설정하기"
categories: gitblog
tag: [gitblog, minimal-mistakes테마]
author_profile: false
description: Minimal Mistakes 지킬(Jekyll) 테마에서 프로필을 설정하는 방법을 알아보겠습니다.
---

Minimal Mistakes 테마의 프로필을 수정해 보자.

<br>
<br>
<br>

## 1. 이름 수정

`_config.yml` 파일의 `# Site Author` 그룹에서 프로필을 수정할 수 있다.  
프로필 이름은 `name`에 입력한다.

```html
name: "Dunku"
```

<br>
<br>
<br>

## 2. 아바타 이미지 추가

`avatar`에 아바타 이미지가 저장된 경로와 파일명을 입력한다.  
아바타 이미지는 `images` 폴더를 생성한 뒤, `dunku_dev_profile.png`로 저장하였다.

```html
avatar: "images/dunku_dev_profile.png"
```

<br>
<br>
<br>

## 3. 블로그 설명

`bio`에 자기 소개나 블로그에 대한 간략한 설명을 입력한다.

```html
bio: "게임 ∙ 웹 코딩 언어 및 엔진 스터디"
```

<br>
<br>
<br>

## 4. 위치 설정

`location`에 현재 거주 중인 곳의 국가나 주소 등을 입력한다.

```html
location: "South Korea"
```

<br>
<br>
<br>

## 5. 이메일 ∙ SNS 링크 설정

`email`에 이메일을 입력한다.  

```html
email: "이메일 주소 입력"
```

<br>

그 외 다양한 SNS 링크는 `links`에 입력한다.

```html
links: 
  - label: "Email" 
  icon: "fas fa-fw fa-envelope-square"
  url: "https://github.com/dunkublog"
```
