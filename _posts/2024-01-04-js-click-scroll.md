---
layout: single
title: "자바스크립트로 메뉴바 요소 클릭하여 스크롤 이동하기"
categories: javascript
tag: [javascript]
author_profile: false
description: 자바스크립트를 활용하여 메뉴바 요소를 클릭하면 브라우저의 스크롤을 특정 위치로 이동시키는 기능을 구현해 보겠습니다.
---

자바스크립트로 메뉴바의 요소를 클릭하면 브라우저의 스크롤을 통해 특정 위치로 이동하는 기능을 구현하자.
<br>
<br>
<br>

## 1. 선행 학습

기능을 구현하기 전에 먼저 알아두어야 할 내용을 알아보자.
<br>

### window.scroll()

브라우저의 스크롤을 특정 위치로 이동시키는 메서드이다.  
사용 문법은 다음과 같다.

```javascript
1. window.scroll(x좌표, y좌표)
2. window.scroll(options 객체)
```

위의 2가지 문법 중에서 2번 문법으로 실습해 보자.
<br>

### HTML 요소의 offsetTop 속성

`offsetTop` 속성은 해당 요소의 윗면이 브라우저 화면 최상단에서 떨어져 있는 거리를 반환해 주는 속성이다.
<br>
<br>

## 2. 기능 구현

위의 내용을 바탕으로 스크롤 기능을 구현하면 다음과 같다.
<br>

### 코드 예제

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZEPQGmB" data-user="blog-dunku" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/blog-dunku/pen/ZEPQGmB">
  자바스크립트로 스크롤 구현</a> by blog dunku (<a href="https://codepen.io/blog-dunku">@blog-dunku</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
<br>

**JavsScript 코드 설명**  
메뉴바 네비 요소의 `onclick` 이벤트에 각 콘텐츠의 윗면 좌표로 스크롤하는 기능을 이벤트로 추가한다.

1. `spans` 변수에 메뉴바의 네비 요소들을 저장한다.
2. `contents` 변수에 실제 콘텐츠 요소들을 저장한다.
3. `topOne, topTwo, topThree` 변수에 각 콘텐츠의 윗면 좌표를 저장한다.
4. 각 네비 요소에 `onclick` 이벤트로 스크롤 함수를 작성하여 저장한다.
5. 스크롤 함수는 `window.scroll` 메서드를 사용한다.
6. `window.scroll` 메서드의 options 객체로 `top` 키에 이동할 위치인 `topOne, topTwo, topThree` 변수를 입력하고, `behavior` 키에 `smooth`를 입력하여 스크롤이 부드럽게 이루어지도록 한다.
   <br>

**TIP**

1. 상하 스크롤이 아닌 좌우 스크롤은 `top` 키 대신 `left` 키를 사용한다.
2. `behavior` 키에 `auto`를 입력하면, 즉각 해당 위치로 이동한다.
