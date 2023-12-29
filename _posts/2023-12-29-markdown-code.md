---
layout: single
title:  "마크다운 코드 ∙ 인용"
categories: markdown
tag: [markdown]
author_profile: false
---

## 1. 목표
마크다운 문법으로 코드와 인용문을 넣어보자.
<br>
<br>
<br>



## 2. 인라인 코드
인라인 형태의 코드는 백틱 기호 <code>`</code>로 해당 코드를 감싸준다.
<br>

### 코드 예제
![마크다운 인라인 코드](https://drive.google.com/uc?export=view&id=13t12S-feXbS7dKLsudaC4btijzyJM2Sl)
<br>

### 결과
문장에 인라인 코드 `console.log('your message')` 삽입.
<br>
<br>
<br>



## 3. 코드 블록
다수의 코드는 백틱 키를 세 번 입력한 <code>```</code> 기호로 감싸 코드 블록으로 만들어준다.  
앞쪽의 <code>```</code> 기호 뒤에 이런 방식으로 <code>```html</code> 어떤 언어인지 적어주면, 코드 문법이 하이라이트 처리되어 화려해진다.
<br>

### 코드 예제
![마크다운 인라인 코드](https://drive.google.com/uc?export=view&id=1B93dCGSvD5yl7d-1eackGEi4kHRLdL2L)
<br>

### 결과
```html
console.log('your message1')  
console.log('your message2')
```
<br>
<br>
<br>



## 4. 인용
인용문은 문장 앞에 <code>></code> 기호를 입력한다.
<br>

### 코드 예제
```html
> 혁신은 선도자와 추종자를 구별 짓는다 -스티브 잡스-
```
<br>

### 결과
> 혁신은 선도자와 추종자를 구별 짓는다 -스티브 잡스-

<br>
<br>


### 코드 예제
<code>></code> 기호를 여러 개 입력하여 인용문의 레벨을 설정한다.
{: .notice}

```html
> 혁신은 선도자와 추종자를 구별 짓는다 -스티브 잡스-
>> 한 번의 홈런이 두 번의 안타보다 훨씬 낫다 -스티브 잡스-
```
<br>

### 결과
> 혁신은 선도자와 추종자를 구별 짓는다 -스티브 잡스-
>> 한 번의 홈런이 두 번의 안타보다 훨씬 낫다 -스티브 잡스-

<br>
<br>


### 코드 예제
인용문 내에서는 마크다운 문법이 그대로 적용된다.
{: .notice}

```html
> **혁신**은 선도자와 추종자를 구별 짓는다 -스티브 잡스-
>> 한 번의 홈런이 두 번의 안타보다 훨씬 낫다 -스티브 잡스-
```
<br>

### 결과
> **혁신**은 선도자와 추종자를 구별 짓는다 -스티브 잡스-
>> 한 번의 홈런이 두 번의 안타보다 훨씬 낫다 -스티브 잡스-
