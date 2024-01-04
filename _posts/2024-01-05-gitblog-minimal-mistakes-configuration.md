---
layout: single
title: "깃허브 블로그 Minimal Mistakes 테마 기본 설정하기"
categories: gitblog
tag: [gitblog]
author_profile: false
description: Minimal Mistakes 지킬(Jekyll) 테마에서 기본적으로 설정해야 하는 사항들을 살펴보겠습니다.
---

`_config.yml` 파일을 수정하여 Minimal Mistakes 테마의 기본 설정을 진행해보자.

<br>
<br>
<br>

## 1. 스킨 변경

`_config.yml` 파일의 `minimal_mistakes_skin` 부분에서 스킨을 변경할 수 있다.  
`air, aqua, contrast, dark, dirt, neon, mint, plum, sunrise` 스킨을 지원하며, [스킨 미리보기](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#skin){:target="\_blank"}에서 스킨을 확인할 수 있다.  
여기서는 `mint` 스킨을 사용하도록 한다.

```html
minimal_mistakes_skin : "mint" # "air", "aqua", "contrast", "dark", "dirt",
"neon", "mint", "plum", "sunrise"
```

<br>
<br>
<br>

## 2. 사이트 설정

`# Site Settings` 그룹에서 사이트의 기본 설정을 진행한다.

### 2-1. 기본 언어 설정

사이트에서 사용할 기본 언어를 설정한다.  
각 나라의 국가 코드는 [국가 코드 테이블](<https://learn.microsoft.com/en-us/previous-versions/commerce-server/ee825488(v=cs.20)>){:target="\_blank"}을 참고한다.
여기서는 한국의 국가 코드인 `ko-KR`를 입력한다.

```html
locale: "ko-KR"
```

<br>
<br>
