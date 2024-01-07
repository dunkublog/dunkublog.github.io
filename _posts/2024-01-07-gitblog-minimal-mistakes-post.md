---
layout: single
title: "깃허브 블로그 Minimal Mistakes 테마 포스트 작성 ∙ 발행"
categories: gitblog
tag: [gitblog, minimal-mistakes테마]
author_profile: false
description: Minimal Mistakes 지킬(Jekyll) 테마에서 포스트를 작성하고, 발행하는 과정을 살펴보겠습니다.
---

Minimal Mistakes 테마에서 포스트를 작성하고, 발행해 보자.

<br>
<br>
<br>



## 1. 포스트 작성

### 포스트 파일 생성

`_post` 폴더에 `날짜-포스트이름.md`의 파일명으로 포스트 작성을 위한 파일을 생성한다.

- 예: _posts/2024-01-03-newpost.md

<br>
<br>


### 포스트 설정값 입력

최상단에 포스트의 레이아웃, 제목, 카테고리, 태그 등의 설정값을 입력한다.

```html
---
layout: post
title:  "포스트의 제목 작성"
categories: 카테고리1
tag: [태그1, 태그1]
author_profile: false
description: 미리 보기 텍스트 작성
---
```

<br>

#### layout
포스트의 레이아웃 형식을 설정한다.  
보통 `post` 또는 `single`로 설정한다.  
레이아웃 종류는 `_layouts` 폴더에서 확인할 수 있다.

<br>

#### Title
현재 포스트의 제목을 입력한다.  
제목은 `<h1>` 태그로 자동 생성된다.  

<br>

#### Category
현재 포스트가 속해있는 카테고리를 설정한다.  

<br>

#### tag
현재 포스트에 태그를 붙인다.  
배열`[]` 안에 `,`로 구분 지어서 복수의 태그를 설정할 수 있다.  

<br>

#### author_profile
포스트에 프로필을 노출시킬 말지 설정한다. 

<br>

#### description
사이트의 메인 화면과 웹브라우저에 보여지는 미리 보기 텍스트를 작성한다.

<br>
<br>


### 포스트 작성

포스트 내용은 마크다운 문법으로 작성한다.  
마크다운 문법은 아래의 링크를 통해 학습할 수 있다.

[▶ 마크다운 문법 스터디](https://dunkublog.github.io/categories/#markdown)
{:target="_blank"}

<br>
<br>


### 포스트 작성일 추가

포스트의 작성일이 디폴트로 보이게 하려면, `_config.yml`을 수정해야 한다.  
`# Defaults` 그룹의 하위 그룹 `# _posts`에 `show_date: true`를 추가한다.  
날짜의 형식은 `# Defaults` 그룹 밑에 한 줄 띄어서 원하는 `date_format` 옵션을 설정한다. (옵션 값은 [Ruby Date Format Cheatsheet](https://www.shortcutfoo.com/app/dojos/ruby-date-format-strftime/cheatsheet){:target="_blank"} 참고)

```html
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: # true
      share: true
      related: true
      show_date: true

date_format: "%y-%m-%d"
```
