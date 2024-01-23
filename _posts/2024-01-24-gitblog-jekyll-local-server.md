---
layout: single
title: "Jekyll 깃허브 블로그 로컬에서 테스트하는 방법"
categories: gitblog
tag: [gitblog, jekyll]
author_profile: false
description: Jekyll로 만든 깃허브 블로그를 로컬에서 테스트하는 방법을 살펴보겠습니다.
---

Jekyll로 깃허브 블로그를 만드는 과정에서 작업 내용을 로컬에서 미리 테스트해 보기 위한 환경을 세팅해 보고자 한다.

참고로, 현재 사용 중인 OS는 Windows 10이다.
<br>
<br>
<br>





## 로컬 테스트 환경 세팅

#### 1. Git 설치하기

[Git for Windows](https://gitforwindows.org/){:target="_blank"}를 설치한다.

<br>

#### 2. Ruby 설치하기

[Ruby for Windows](https://rubyinstaller.org/){:target="_blank"}를 설치한다.  


설치가 완료되면, 커맨드 창을 열고 `ruby -v` 명령어를 입력하여 Ruby가 제대로 설치되었는지 확인할 수 있다.

```html
c:\>ruby -v
ruby 3.2.2 (2023-03-30 revision e51014f9c0) [x64-mingw-ucrt]
```

<br>

#### 3. Jekyll 설치하기

커맨드 창에 `gem install jekyll bundler` 명령어를 입력한다.

```html
c:\>gem install jekyll bundler
```

<br>

`jekyll -v` 명령어로 Jekyll이 제대로 설치되었는지 확인할 수 있다. 

```html
c:\>jekyll -v
jekyll 4.3.3
```

<br>

#### 4. 로컬에 띄우기

커맨드 창에 작업 중인 지킬 블로그의 로컬 경로로 이동한다.

참고로, 나의 경우에는 F 드라이버에 `GitBlog\testblog` 폴더가 작업 중인 지킬 블로그의 로컬 경로이다.

```html
c:\>f:

F:\>cd GitBlog\testblog

F:\GitBlog\testblog>
```

<br>

커맨드 창에 `jekyll serve` 명령어를 입력한다.

해당 명령어가 실행되지 않으면, `bundle exec jekyll serve` 명령어를 시도해 보자.

```html
F:\GitBlog\testblog>jekyll serve
```

<br>

마지막에 아래와 같은 화면이 나오면 로컬 서버에 연결된 것이다.

```html
Run in verbose mode to see all warnings.
          Conflict: The following destination is shared by multiple files.
                    The written file may end up with unexpected contents.
                    F:/GitBlog/testblog/_site/index.html
                     - index.html
                     - index.markdown

                    done in 1.036 seconds.
 Auto-regeneration: enabled for 'F:/GitBlog/testblog'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

<br>

커맨드 창을 닫지 말고, 크롬 웹브라우저에 `http://127.0.0.1:4000/`를 입력하면 작업 중인 지킬 블로그의 화면을 확인할 수 있다.
