---
layout: single
title:  "마크다운 이미지 ∙ 링크"
categories: markdown
tag: [markdown]
author_profile: false
---

## 1. 목표
마크다운 문법으로 이미지와 링크를 추가해보자.
<br>
<br>
<br>



## 2-1. 이미지 삽입
`![이미지 설명](이미지 URL)`로 이미지를 삽입한다.
<br>

### 코드 예제
```html
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ)
```
<br>

### 결과
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ)
<br>
<br>
<br>



## 2-2. 이미지 리사이즈
이미지 URL 뒤에 `{: width="가로크기" height="세로크기"}`를 추가하여 사이즈를 조절할 수 있다.
<br>

### 코드 예제
`px`을 단위로 사용할 수 있으며, 생략이 가능하다.
{: .notice}

```html
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ){: width="300" height="300"}
```
<br>

### 결과
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ){: width="300" height="300"}
<br>
<br>


### 코드 예제
`%`도 단위로 사용할 수 있다. 주의할 점은 화면을 차지하는 비율을 기준으로 한다.
{: .notice}

```html
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ){: width="50%" height="50%"}
```
<br>

### 결과
![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ){: width="50%" height="50%"}
<br>
<br>
<br>



## 3-1. URL 링크
링크할 사이트의 URL 주소나 e메일 주소를 직접 입력한다.  
꺽쇠 기호 <code><></code>로 감싸 명시할 수도 있다.
<br>

### 코드 예제
```html
https://github.com/
<https://github.com>
```
<br>

### 결과
https://github.com/
<https://github.com>
<br>
<br>
<br>



## 3-2. 텍스트 링크
`[텍스트](URL)`로 텍스트에 링크를 삽입한다.
<br>

### 코드 예제
```html
[깃허브](https://github.com)는 깃 저장소 호스팅을 지원하는 웹 서비스이다.
```
<br>

### 결과
[깃허브](https://github.com)는 깃 저장소 호스팅을 지원하는 웹 서비스이다.
<br>
<br>


### 코드 예제
주소 옆에 <code>""</code>로 title(설명)을 추가할 수 있다.  
마우스 포인터를 갖다대면, 타이틀을 확인할 수 있다.
{: .notice}

```html
[깃허브 홈페이지 바로가기](https://github.com "깃 저장소 호스팅을 지원하는 웹 서비스")
```
<br>

### 결과
[깃허브 홈페이지 바로가기](https://github.com "깃 저장소 호스팅을 지원하는 웹 서비스")
<br>
<br>
<br>



## 3-3. 참조 링크
참조 링크는 동일한 링크를 여러 번 사용할 때 유용하다.  
`[참조텍스트]: URL` 형태로 참조할 링크를 미리 준비해두고, '참조텍스트'로 링크를 호출한다.
<br>

### 코드 예제
주소 옆에 <code>""</code>로 title(설명)을 추가할 수 있다.  
마우스 포인터를 갖다대면, 타이틀을 확인할 수 있다.
{: .notice}

```html
[깃허브 홈페이지][참조 URL] 텍스트에 사용할 수 있다.  
문장 안에서도 [참조 URL1] 사용할 수 있다.  
title(설명)을 [참조 URL2] 추가할 수 있다.

[참조 URL1]: https://github.com
[참조 URL2]: https://github.com "깃 저장소 호스팅을 지원하는 웹 서비스"
```
<br>

### 결과
[깃허브 홈페이지][참조 URL] 텍스트에 사용할 수 있다.  
문장 안에서도 [참조 URL1] 사용할 수 있다.  
title(설명)을 [참조 URL2] 추가할 수 있다.

[참조 URL1]: https://github.com
[참조 URL2]: https://github.com "깃 저장소 호스팅을 지원하는 웹 서비스"
<br>
<br>
<br>



## 3-3. 이미지 링크
`[![이미지 설명(이미지 URL)]](링크 URL)`로 이미지에 링크를 삽입할 수 있다.
<br>

### 코드 예제
주소 옆에 <code>""</code>로 title(설명)을 추가할 수 있다.  
마우스 포인터를 갖다대면, 타이틀을 확인할 수 있다.
{: .notice}

```html
[![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ)](https://github.com)
```
<br>

### 결과
[![깃허브 로고](https://drive.google.com/uc?export=view&id=16Ku3POM7MhzZkrfzXpOQjXnXkBqFdYfJ)](https://github.com)
