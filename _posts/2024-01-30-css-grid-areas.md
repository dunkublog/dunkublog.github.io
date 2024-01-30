---
layout: single
title: "Grid Areas로 CSS 레이아웃 구성하기"
categories: css
tag: [css]
author_profile: false
description: 아이템을 자유자재로 배치할 수 있는 CSS 레이아웃인 Flex와 Grid의 차이를 알아보고, Grid Areas로 레이아웃을 구성하는 방법을 살펴보겠습니다.
---

Grid Areas로 레이아웃을 구성하는 방법을 알아보자.

<br>
<br>
<br>





## 1. Flex와 Grid의 차이점

### Flex
Flex 박스는 아이템을 가로(행/row) 또는 세로(열/column) 중 한 방향으로 1차원적으로 배치할 수 있게 도와준다.

<br>



### Grid
Grid는 아이템을 가로축과 세로축의 2차원적으로 배치할 수 있게 도와준다.

<br>
<br>
<br>





## 2. Grid 개념

### grid와 grid cell

부모 컨테이너에 `display: grid`로 그리드를 지정해 주면, 그리드 안에 들어있는 자식 요소들은 모두 그리드의 셀로 변환된다.

<br>

grid
| grid cell | grid cell | grid cell |
|    ---    |    ---    |    ---    |
| grid cell | grid cell | grid cell |
| grid cell | grid cell | grid cell |

<br>
<br>
<br>





## 3. Grid Areas로 레이아웃 구성하기

그리드 레이아웃 방식에는 여러 가지가 있지만, 여기서는 Grid Areas로 레이아웃을 구성하는 방법을 알아본다.

<br>
<br>



### grid

부모 컨테이너인 grid는 그리드의 전체적인 모양이나 사이즈를 지정할 수 있다.

<br>

#### grid-areas

강력한 그리드 방식으로, 템플릿 영역에 이름을 지정하여 아이템을 배치할 수 있다.

<br>

#### grid-gap

그리드 셀 사이의 간격을 지정할 수 있다. `grid-column-gap` 또는 `grid-row-gap`을 사용하면, 행과 열에 개별적으로 간격을 줄 수 있다.

<br>
<br>



### grid cell

그리드 안에 들어있는 각각의 그리드 셀은 자신이 그리드 내에서 몇 개의 셀을 차지하고, 어떤 셀에 표기가 될 것인지 지정할 수 있다.

<br>

#### grid-area

지정해둔 템플릿 영역 이름을 통해 어떤 영역에 보일 것인지 지정할 수 있다.

<br>
<br>



### 실습

#### 실습 1

| A | A | A |
|---|---|---|
| B | C | C |
| B | D | E |

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="YzgeyOa" data-user="blog-dunku" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/blog-dunku/pen/YzgeyOa">
  Grid Areas 1</a> by blog dunku (<a href="https://codepen.io/blog-dunku">@blog-dunku</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

#### 실습 2

| A | A | C |
|---|---|---|
| E | D | C |
| B | B | C |

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxBYwQr" data-user="blog-dunku" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/blog-dunku/pen/xxBYwQr">
  Grid Areas 2</a> by blog dunku (<a href="https://codepen.io/blog-dunku">@blog-dunku</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

#### 실습 3

| Header | Header |
| ---    | ---    |
| Nav    | Main   |
| Nav    | Footer |

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="MWxQwdR" data-user="blog-dunku" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/blog-dunku/pen/MWxQwdR">
  Grid Areas</a> by blog dunku (<a href="https://codepen.io/blog-dunku">@blog-dunku</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
