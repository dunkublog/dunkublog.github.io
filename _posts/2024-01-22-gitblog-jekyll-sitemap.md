---
layout: single
title: "Jekyll 깃허브 블로그에 플러그인 없이 Sitemap 만드는 방법"
categories: gitblog
tag: [gitblog, jekyll]
author_profile: false
description: Jekyll로 만든 깃허브 블로그에서 별도의 플러그인을 사용하지 않고 Sitemap을 만드는 방법을 살펴보겠습니다.
---

Jekyll로 만든 깃허브 블로그(Github-Pages)에서 sitemap을 만드는 방법을 살펴보자.

웹사이트의 검색 봇이 내 글을 주기적으로 크롤링 하려면 Google, Naver, Daum 검색엔진에 sitemap을 등록해야 한다.
<br>
<br>
<br>





## Sitemap 만드는 방법

깃허브 블로그(Github-Pages)에서는 플러그인이 작동하지 않는 경우가 종종 발생하기 때문에, Jekyll plgin-in을 사용하지 않고 sitemap.xml을 직접 만들어 사용하는 것이 나을 수 있다.

<br>



### sitemap.xml 파일 만들기

깃허브 블로그 루트 디렉터리에 sitemap.xml 파일을 생성한 다음, sitemap.xml 파일에 아래의 코드를 붙여넣고 저장한다.

<br>


#### sitemap.xml 파일 내용

{% raw %}
```html
---
layout: null
---
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd" xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  {% for page in site.pages %}
  {% if page.url contains '.xml' %}{% else %}
      <url>
        <loc>{{ site.url }}{{ page.url }}</loc>
        <changefreq>monthly</changefreq>
        <priority>1.0</priority>
       </url>
  {% endif %}
  {% endfor %}
  {% for page in site.posts %}
      <url>
        <loc>{{ site.url }}{{ page.url | replace: 'index.html', '' }}</loc>
        <changefreq>monthly</changefreq>
        <priority>1.0</priority>
       </url>
  {% endfor %}
</urlset>
```
{% endraw %}

<br>

`head` 부분에 다음 줄을 추가하고, 각 검색 엔진에 sitemap.xml 파일을 등록한다.

{% raw %}
```html
<link rel="sitemap" type="application/xml" title="Sitemap" href="/sitemap.xml" />
```
{% endraw %}

참고 자료: [Jekyll 코드샘플 사이트](https://jekyllcodex.org/without-plugin/sitemap/){:target="_blank"}
