---
layout: single
title: "Jekyll 깃허브 블로그에 플러그인 없이 RSS Feed 만드는 방법"
categories: gitblog
tag: [gitblog, jekyll]
author_profile: false
description: Jekyll로 만든 깃허브 블로그에서 별도의 플러그인을 사용하지 않고 RSS Feed를 만드는 방법을 살펴보겠습니다.
---

Jekyll로 만든 깃허브 블로그(Github-Pages)에서 RSS Feed를 만드는 방법을 살펴보자.

웹사이트에서 내 글이 검색될 확률을 높이기 위하여 Google, Naver, Daum 검색엔진에 RSS를 등록해야 한다.

<br>
<br>
<br>





## RSS Feed 만드는 방법

깃허브 블로그(Github-Pages)에서는 플러그인이 작동하지 않는 경우가 종종 발생하기 때문에, Jekyll plgin-in을 사용하지 않고 feed.xml을 직접 만들어 사용하는 것이 나을 수 있다.

<br>



### feed.xml 파일 만들기

깃허브 블로그 루트 디렉터리에 feed.xml 파일을 생성한 다음, feed.xml 파일에 아래의 코드를 붙여넣고 저장한다.

#### feed.xml 파일 내용

{% raw %}
```html
---
layout: null
---
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
  <channel>
    <title>{{ site.title | xml_escape }}</title>
    <description>{{ site.description | xml_escape }}</description>
    <link>{{ site.url }}{{ site.baseurl }}/</link>
    <atom:link href="{{ "/feed.xml" | prepend: site.baseurl | prepend: site.url }}" rel="self" type="application/rss+xml"/>
    <pubDate>{{ site.time | date_to_rfc822 }}</pubDate>
    <lastBuildDate>{{ site.time | date_to_rfc822 }}</lastBuildDate>
    <generator>Jekyll v{{ jekyll.version }}</generator>
    {% for post in site.posts limit:10 %}
      <item>
        <title>{{ post.title | xml_escape }}</title>
        <description>{{ post.content | xml_escape }}</description>
        <pubDate>{{ post.date | date_to_rfc822 }}</pubDate>
        <link>{{ post.url | prepend: site.baseurl | prepend: site.url }}</link>
        <guid isPermaLink="true">{{ post.url | prepend: site.baseurl | prepend: site.url }}</guid>
        {% for tag in post.tags %}
        <category>{{ tag | xml_escape }}</category>
        {% endfor %}
        {% for cat in post.categories %}
        <category>{{ cat | xml_escape }}</category>
        {% endfor %}
      </item>
    {% endfor %}
  </channel>
</rss>
```
{% endraw %}

<br>

`head` 부분에 다음 줄을 추가하고, 각 검색 엔진에 feed.xml 파일을 등록한다.

{% raw %}
```html
<link rel="alternate" type="application/rss+xml" href="{{ site.url }}/feed.xml">
```
{% endraw %}

참고 자료: [Jekyll 코드샘플 사이트](https://jekyllcodex.org/without-plugin/rss-feed/){:target="_blank"}
