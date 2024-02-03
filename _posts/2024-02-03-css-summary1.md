---
layout: single
title: "CSS 요점 정리 I (적용 방법, 선택자, 폰트, 텍스트, 배경)"
categories: css
tag: [css]
author_profile: false
description: CSS에 사용되는 주요한 내용들 중에서 선택자, 폰트, 텍스트, 배경과 관련된 내용의 요점만 모아서 정리해 보았습니다. 
---

CSS '선택자, 폰트, 텍스트, 배경'의 핵심 내용을 정리해 보자.

<br>
<br>
<br>





## CSS 적용 방법

CSS는 HTML 문서의 스타일을 꾸밀 때 사용하는 스타일 시트 언어이다. CSS 파일을 적용하는 방법에는 다음과 같은 3가지가 있다.

<br>

**Inline CSS**

html 문서에 작성된 요소에 직접 CSS 스타일을 작성한다.

<br>

**Internal CSS**

html 문서의 head 영역에 `<style>` 태그로 CSS 스타일을 작성한다.

<br>

**External CSS**

외부에 작성한 CSS 파일을 `<link>` 태그로 html 파일에 연결한다.

<br>
<br>
<br>





## 선택자

선택자란 스타일을 적용할 대상 요소를 선택해 주는 도구로, 다음과 같은 다양한 선택자가 있다.

<br>

**전체 선택자(Universal Selector)**

HTML 페이지의 모든 요소(태그)를 선택한다.

```html
* { margin: 0; }
```

<br>

**태그 선택자(Type Selector)**

특정 태그를 선택한다.

```html
p { color: black; }
```

<br>

**클래스 선택자(Class Selector)**

특정 클래스를 선택한다.

```html
.클래스명 { color: black; }
```

<br>

**ID 선택자(ID Selector)**

특정 ID를 선택한다.

```html
#ID명 { color: black; }
```

<br>

**복합 선택자(Combinator)**

두 개 이상의 선택자를 사용하여 요소를 선택한다.

- **하위 선택자:** 모든 하위 요소를 선택한다.
  - `상위요소 하위요소`
```html
div ul { border: 1px solid black; }
```

<br>

- **자식 선택자:** 자식 요소를 선택한다.
  - `부모요소>자식요소1`
```html
div>ul { border: 1px solid black; }
```

<br>

- **형제 선택자:** 모든 형제 요소를 선택한다.
  - `요소1~요소2`
```html
h1~ul { border: 1px solid black; }
```

<br>

- **인접 형제 선택자:** 가장 가까운 형제 요소만 선택한다.
  - `요소1+요소2`
```html
h1+ul { border: 1px solid black; }
```

<br>

**속성 선택자(Attribute Selectors)**

요소(태그) 안의 특정 속성들에 따라 스타일을 지정한다. 속성 값의 조건에 따라 스타일을 다양하게 지정할 수 있어 활용도가 높다.

- **`요소[속성]`:** 속성이 포함된 요소를 선택한다.
- **`요소[속성 = "값"]`:** 속성의 값이 지정한 값과 일치하는 요소를 선택한다.
- **`요소[속성 ~= "값"]`:** 속성의 값에 지정한 값이 포함되는 요소를 선택한다. (공백도 체크)
- **`요소[속성 ^= "값"]`:** 속성의 값이 지정한 값으로 시작되는 요소를 선택한다.
- **`요소[속성 $= "값"]`:** 속성의 값이 지정한 값으로 끝나는 요소를 선택한다.
- **`요소[속성 *= "값"]`:** 속성의 값에 지정한 값이 포함되는 요소를 선택한다.
- **`요소[속성 |= "값"]`:** 속성의 값이 지정한 값이거나 지정한 값으로 시작되는 요소를 선택한다.

```html
<!-- 요소[속성] 형식 -->
a[href] { color : black; }

<!-- 요소[속성 = "값"] 형식 -->
input[type="text"] { width: 100px; }

<!-- 요소[속성 $= "값"] 형식 -->
a[href$=".xml"] { background: white; }
```

<br>

**가상 클래스 선택자(Pseudo-Classes)**

링크 선택자 ∙ 동적(이벤트) 선택자
- **`:link`:** 방문하지 않은 링크일 때
- **`:visited`:** 방문한 링크일 때
- **`:active`:** 요소를 마우스 클릭 또는 키보드 엔터가 눌렸을 때
- **`:hover`:** 요소에 마우스 커서를 올렸을 때
- **`:focus`:** 요소에 포커스(초점)가 머물러 있을 때

<br>

UI 요소 상태 선택자
- **`:enabled`:** 폼의 요소가 활성화된(사용 가능한) 상태일 때
- **`:disabled`:** 폼의 요소가 비활성화된(사용 불가능한) 상태일 때
- **`:checked`:** 라디오나 체크박스에서 해당 항목을 선택했을 때

<br>

구조적 가상 클래스 선택자
- **`:root`:** 문서의 최상위 요소를 선택한다.

- **`:nth-child(n)`:** 앞에서부터 n번째 자식 요소를 선택한다.
- **`:nth-last-child(n)`:** 뒤에서부터 n번째 자식 요소를 선택한다.

- **`:nth-of-type(n)`:** 앞에서부터 n번째 요소를 선택한다. (해당 요소의 순서만 계산)
- **`:nth-last-of-type(n)`:** 뒤에서부터 n번째 요소를 선택한다. (해당 요소의 순서만 계산)

- **`:first-child`:** 첫 번째 자식 요소를 선택한다.
- **`:last-child`:** 마지막 자식 요소를 선택한다.

- **`:first-of-type`:** 첫 번째 형제 요소를 선택한다. (해당 요소의 순서만 계산)
- **`:last-of-type`:** 마지막 형제 요소를 선택한다. (해당 요소의 순서만 계산)

- **`:only-child`:** 해당 요소가 부모 요소 안에서 유일한 자식 요소이면 선택한다.
- **`:only-of-type`:** 해당 요소가 형제 요소 중에서 유일한 타입의 요소이면 선택한다.

- **`:empty`:** 텍스트, 공백을 포함하여 자식 요소가 없는 요소를 선택한다.

<br>

가상 요소 선택자  
_가상 요소는 가상 선택자와 구분하기 위해 클론을 두 개(::) 붙인다._
- **`::first-line`:** 지정한 요소의 첫 번째 줄을 선택한다.
- **`::first-letter`:** 지정한 요소의 첫 번째 문자를 선택한다.
- **`::before`:** 지정한 요소의 시작 지점을 선택한다.
- **`::after`:** 지정한 요소의 끝 지점을 선택한다.

<br>

그 외 선택자
- **`:lang(ko)`:** lang 속성의 값이 'ko'인 요소를 선택한다.
- **`:not(S)`:** 괄호 안에 지정한 선택자 이외의 모든 요소를 선택한다.  
- **`:target`:** URL의 해시값과 일치하는 앵커의 목적지인 요소를 선택한다.

<br>
<br>
<br>




## 폰트 관련 속성

- **`font-family`:** 글꼴을 설정한다. 웹 브라우저에 따라 지원되지 않는 글꼴도 있어 지원을 희망하는 순서대로 여러 개의 글꼴을 설정해 주는 것이 좋다.

- **`font-size`:** 글자의 크기를 설정한다.

- **`font-weight`:** 글자의 굵기를 아래의 4가지 값 중에서 하나로 표현한다.
  - lighter
  - normal
  - bold
  - bolder

- **`font-variant`:** 소문자를 작은 사이즈의 대문자로 표현한다.
  - normal
  - small-caps

- **`font-style`:** 글꼴의 스타일을 이탤릭체(italic), 기울임(oblique) 등으로 표현한다.
  - normal
  - italic
  - oblique

- **`font`:** font로 한 번에 지정할 수도 있다. `font: 10px italic bolder;`

- **`color`:** 글자의 색상을 지정한다.

<br>
<br>
<br>





## 텍스트 관련 속성
- **`text-align`:** 텍스트의 정렬 방식을 선택한다.
  - `start`: 글의 시작점 정렬 (left와 같아 보이지만, 글씨 방향이 반대면 차이가 남)
  - `end`: 글의 끝점 정렬 (right와 같아 보이지만, 글씨 방향이 반대면 차이가 남)
  - `left`: 좌정렬
  - `right`: 우정렬
  - `cente`: 중앙 정렬
  - `justify`: 라인 양쪽으로 붙여서 정렬
  - `match-parent`: start, end 속성을 left, right 값으로 치환하여 가져옴
  - `inherit`: 부모에게 상속받음

- **`text-decoration`:** 텍스트의 라인(밑줄, 취소선 등)을 설정한다.
  - `none`: 설정 제거
  - `underline`: 밑줄
  - `overline`: 위에 줄
  - `line-through`: 취소선

- **`text-underline-offset`:** 텍스트의 밑줄의 위치를 설정한다.
- **`text-underline-position`:** 텍스트의 밑줄이 텍스트와 어떻게 상호 작용하는지 설정한다.
  - `auto`: 브라우저가 밑줄 위치를 자동으로 결정
  - `under`: 밑줄을 텍스트의 기준선 아래에 위치

- **`text-shadow`:** 텍스트의 그림자 효과를 설정한다.
  - `none`: 설정 제거  
  - 문법: `text-shadow: 가로위치 세로위치 흐림정도 색상`

- **`text-stroke`:** 텍스트의 외곽선 효과를 설정한다.
  - `text-stroke-width`: 외곽선의 너비를 설정
  - `text-stroke-color`: 외곽선의 색상을 설정

- **`text-transform`:** 텍스트의 대소문자 변환을 설정한다.
  - `none`: 설정 제거
  - `capitalize`: 각 단어의 첫 글자를 대문자로
  - `uppercase`: 텍스트 전체를 대문자로
  - `lowercase`: 텍스트 전체를 소문자로
  - `full-width`: 텍스트 전체를 전각 문자로

- **`text-justify`:** 텍스트의 정렬 및 간격을 설정한다.
  - `auto`: 브라우저의 정렬 방법을 자동으로 설정 (기본값)
  - `none`: 브라우저가 텍스트를 정렬하는 것을 비활성화
  - `distribute`: 줄 사이의 간격을 조절
  - `inter-word`: 단어 사이의 간격을 조절
  - `inter-cluster`: 문자 단위로 간격을 조절
  - `inter-ideograph`: 한자 및 기타 동양 문자 간의 간격을 조절
  - `kashida`: 아랍어 텍스트에서 글자 사이의 간격을 조절

- **`text-indent`:** 텍스트의 들여쓰기 폭을 설정한다.

- **`text-overflow`:** 텍스트가 범위를 넘어갈 때 어떻게 처리할지 설정한다.
  - `clip`: 넘치는 부분을 자름
  - `ellipsis`: 넘치는 부분을 말 줄임표(⋯)로 표시

- **`white-space`:** 요소 내의 공백과 줄 바꿈 처리를 설정한다.
  - `normal`: 연속된 공백을 하나의 공백으로 처리 (기본값)
  - `nowrap`: 공백을 무시하고 텍스트를 한 줄에 표시, 줄바꿈 X
  - `pre`: HTML 소스 코드에서와 같이 공백을 그대로 표시, 줄바꿈 X
  - `pre-wrap`: 연속된 공백을 그대로 표시, 줄바꿈O
  - `pre-line`: 연속된 공백을 하나로 표시, 줄바꿈O

- **`direction`:** 텍스트의 흐름 방향을 설정한다.
  - `ltr`: 왼쪽 → 오른쪽
  - `rtl`: 오른쪽 → 왼쪽

- **`line-height`:** 텍스트 줄의 높이를 설정한다.

- **`letter-spacing`:** 텍스트의 각 문자 사이의 간격을 설정한다.

- **`word-spacing`:** 텍스트 안의 단어 사이의 간격을 설정한다.

<br>
<br>
<br>





## 배경 관련 속성

- **`background-color`:** 요소의 배경색을 설정한다.

- **`background-image`:** 요소의 배경에 이미지를 설정한다.
  - `background-image: url('이미지의 파일 경로 또는 주소');`: 작은따옴표 대신 큰따옴표도 사용 가능하며 생략도 가능

- **`background-repeat`:** 배경 이미지의 반복 방법을 설정한다.
  - `repeat`: 화면에 가득 찰 때까지 수평, 수직으로 반복 (기본값)
  - `repeat-x`: 수평으로만 반복
  - `repeat-y`: 수직으로만 반복
  - `no-repeat`: 한 번만 표시하고 반복하지 않음

- **`background-position`:** 배경 이미지의 위치를 설정한다.
  - 수평: `left`, `center`, `right`, `백분율`, `길이 값`
  - 수직: `top`, `center`, `bottom`, `백분율`, `길이 값`

```html
selector {
  background-image: url('이미지의 파일 경로 또는 주소');
  background-position: right top; /* 우상단 배치 */
}
```

- **`background-attachment`:** 화면을 스크롤 할 때 배경 이미지의 고정 여부를 설정한다.
  - `scroll`: 함께 스크롤 됨
  - `fixed`: 고정됨

- **`background-size`:** 배경 이미지의 크기를 설정한다.
  - `auto`: 원래 크기를 유지
  - `contain`: 요소 안에 들어오도록 이미지를 축소함
  - `cover`: 요소에 맞게 이미지를 늘려서 채우며, 부족한 부분은 자름
  - `크기 값`:  px, % 등 직접 크기를 설정함

- **`background-clip`:** 배경이미지 또는 배경색이 요소의 어느 범위까지 표시될지 설정한다.
  - `border-box`: 테두리 영역까지 적용 (기본값)
  - `padding-box`: 테두리를 제외한 패딩 영역까지 적용
  - `content-box`: 콘텐츠 영역까지만 적용

- **`background-origin`:** 배경 이미지의 원점(시작 위치)을 설정한다.
  - `border-box`: 테두리 영역을 기준으로 배치됨
  - `padding-box`: 패딩 영역을 기준으로 배치됨
  - `content-box`: 콘텐츠 영역을 기준으로 배치됨

- **`background`:** 한 줄로 위의 속성들을 적용할 수 있다.

```html
background: blue url() center;
```

- **`그라데이션 효과`:** 선형, 원형 2가지 방식으로 그라데이션 효과를 줄 수 있다.
  - 선형 그라데이션: `linear-gradient(각도/방향, color-stop1, ... color-stopN);`
  - 원형 그라데이션: `radial-gradient(모양/크기/위치, color-stop1, ... color-stopN);`

```html
selector1 {
  background-image: linear-gradient(45deg, red, green);
  background-image: linear-gradient(to right, red , green);
}

selector2 {
  background-image: radial-gradient(red, green, blue);
  background-image: radial-gradient(circle, red, green, blue);
  background-image: radial-gradient(farthest-side at 60% 55%, red, green, blue);
}
```
