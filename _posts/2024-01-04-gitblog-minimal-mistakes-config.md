---
layout: single
title: "깃허브 블로그 Minimal Mistakes 테마 기본 설정하기"
categories: gitblog
tag: [gitblog]
author_profile: false
description: Minimal Mistakes 지킬(Jekyll) 테마에서 기본적으로 설정해야 하는 사항들을 살펴보겠습니다.
---

Minimal Mistakes 테마의 기본 설정을 진행해 보자.

<br>
<br>
<br>

## 1. 스킨 변경

`_config.yml` 파일의 `minimal_mistakes_skin` 부분에서 스킨을 변경할 수 있다.  
`air, aqua, contrast, dark, dirt, neon, mint, plum, sunrise` 스킨을 지원하며, [스킨 미리 보기](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#skin){:target="\_blank"}에서 스킨을 확인할 수 있다.  
여기서는 `mint` 스킨을 사용하도록 한다.

```html
minimal_mistakes_skin : "mint" # "air", "aqua", "contrast", "dark", "dirt",
"neon", "mint", "plum", "sunrise"
```

<br>
<br>
<br>

## 2. 사이트 기본 설정

`# Site Settings` 그룹에서 사이트의 기본 설정을 진행한다.

<br>
<br>

### 기본 언어 설정

`locale`에 사이트에서 사용할 기본 언어를 설정한다.  
각 나라의 국가 코드는 [국가 코드 테이블](<https://learn.microsoft.com/en-us/previous-versions/commerce-server/ee825488(v=cs.20)>){:target="\_blank"}을 참고한다.  
여기서는 한국의 국가 코드인 `ko-KR`를 입력한다.

```html
locale: "ko-KR"
```

<br>
<br>

### 사이트 이름 설정

`title`에 사이트의 이름을 입력한다.

```html
title: "Dunku DEV"
```

<br>

`title_separator`에 SEO 친화적인 페이지 제목 구분 문자로 `|`를 설정한다.

```html
title_separator: "|"
```

<br>

`subtitle`에 `title` 아래에 출력되는 짧은 태그라인을 입력한다.

```html
subtitle: "Coding Study Blog"
```

<br>
<br>

### 사이트 작성자 이름 설정

`name`에 사이트 작성자의 이름을 입력한다.  
각 게시물의 작성자는 따로 재정의할 수 있다.

```html
name: "Dunku"
```

<br>
<br>

### 사이트 설명 작성

`description`에 사이트에 대한 간략한 설명을 작성한다.
`description`은 SEO 개선을 ​​위한 '메타 디스크립션'으로 사용된다.

```html
description: "유니티, c#, html, css, 자바스크립트 등 코딩과 관련된 다양한 언어
및 엔진을 공부합니다."
```

<br>
<br>

### 사이트 url 설정

`url`에 사이트의 url을 입력한다.  
`baseurl`는 의도치 않은 문제를 야기할 수 있기 때문에 되도록 사용하지 않는다.

간혹, 'Minimal Mistakes'가 `baseurl`가 있는 경우가 있는데, 되도록 사용하지 말자.
{: .notice--danger}

```html
url: "https://dunkublog.github.io"
```
