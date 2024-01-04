---
layout: single
title: "깃허브 블로그 지킬(Jekyll) 테마로 손쉽게 만들기"
categories: gitblog
tag: [gitblog]
author_profile: false
description: 깃허브를 손쉽게 만들 수 있는 방법으로 지킬(Jekyll) 테마를 사용하는 방법에 대해 알아보겠습니다.
---

지킬(Jekyll) 테마를 사용하여 깃허브 블로그를 10분 만에 세팅해 보자.

<br>
<br>
<br>

## 1. 깃허브 블로그를 선택한 이유

네이버, 티스토리, 브런치, 블로그 스팟 등 다양한 블로그 사이트가 있지만, 그 중에서 깃허브 블로그를 선택한 이유는 다음과 같다.

- 블로그를 내가 원하는 방향으로 마음대로 만들 수 있음
- 호스팅 비용이 들지 않음
- 애드센스로 수익창출이 가능함

<br>
<br>
<br>

## 2. 깃허브 블로그 만들기

### 2-1. 깃허브 계정 생성

[깃허브 홈페이지](https://github.com/){:target="\_blank"}에 접속하여 계정을 생성한다.

<br>
<br>

### 2-2. 지킬 테마 적용

**테마 선택**

1. [지킬 테마](https://github.com/topics/jekyll-theme){:target="\_blank"} 사이트에 접속하여 원하는 테마를 선택한다.
2. 여기서는 Star를 가장 많이 받은 [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes){:target="\_blank"} 테마를 선택했다.

<br>

**테마 적용**

1. 선택한 테마를 적용하려면, [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes){:target="\_blank"} 테마 우측 상단의 Fork를 클릭한다.
2. Fork가 완료되면, Settings 탭을 클릭하여 설정 페이지로 넘어간다.
3. 리파지토리의 이름을 변경해야 하는데, Repository name에 반드시 `사용자ID.github.io` 형식으로 이름은 입력한 다음 Rename 버튼을 클릭한다.
4. 테마의 url 설정을 위해 \_config.yml 파일을 클릭한다.
5. 연필 모양의 아이콘(Edit this File)을 클릭한다.
6. 주석 처리되어 있는 url을 `"https://사용자ID.github.io"`로 수정한 뒤, Commit changes 버튼을 클릭한다.
7. 수정한 url에 접속해 보면, 테마가 적용된 깃허브 블로그를 확인할 수 있다.

<br>
<br>

### 2-3. 첫 포스트 발행

1. 깃허브 블로그 리파지토리의 Add file → Create new file을 클릭한다.
2. Name your file...에 `_posts/2024-01-03-newpost.md` 형식으로 포스트용 파일을 생성한다. 반드시 `_posts` 경로 밑에 `날짜-포스트이름.md`로 파일명을 작성해야 한다.
3. 포스트 내용을 작성하기 전에 상단에 아래의 코드를 입력한다.

```
---
layout: post
title:  "여기에 포스트 제목 작성."
---
```

4. 실제 포스트 내용은 마크다운 문법으로 작성한다.
5. 마크다운 문법은 아래의 링크를 통해 학습할 수 있다.

<br>

[▶ 마크다운 문법 스터디](https://dunkublog.github.io/categories/#markdown)
