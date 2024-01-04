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

- 깃허브 블로그 리파지토리의 Add file → Create new file을 클릭한다.
- Name your file...에 `_posts/2024-01-03-newpost.md` 형식으로 포스트용 파일을 생성한다. 반드시 `_posts` 경로 밑에 `날짜-포스트이름.md`로 파일명을 작성해야 한다.
- 포스트 내용을 작성하기 전에 상단에 아래의 코드를 입력한다.

```
---
layout: post
title:  "여기에 포스트 제목 작성."
---
```

- 실제 포스트 내용은 마크다운 문법으로 작성한다.
- 마크다운 문법은 아래의 링크를 통해 학습할 수 있다.

<br>

[▶ 마크다운 문법 스터디](https://dunkublog.github.io/categories/#markdown)
