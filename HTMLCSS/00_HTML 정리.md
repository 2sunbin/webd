# 📃 HTML

<details>
<summary>목차</summary>

[1. HTML이란 무엇일까요?](#1-html이란-무엇일까요?)

- [1-1. HTML의 기본 구성](#1-1-html의-기본-구성)

[2. HTML의 태그](#2-HTML의-태그)

- [2-1. 글자/폰트 태그](#2-1.-글자/폰트-태그)

</details>

<br>

---
---

> ## 1. HTML이란 무엇일까요?

- 웹 브라우저에 표시되도록 설계된 문서의 표준 마크업 언어
    ##### 마크업 언어 : 태그 등을 이용해 문서나 데이터의 구조를 명시하기 위한 규칙을 정리한 언어
        

>> ### 1-1. HTML의 기본 구성

|요소|의미|예시|
|----|----|----|
|태그(tag)|'<>'로 둘러싸인 문자열로 시작태그(<>)와 종료태그(</>)로 구성|**<h1<k>></h1<k>>**|
|내용(content)|태그로 둘러싸인 문자열|<h1<k>>**Hi**</h1<k>>|
|엘리먼트(element)|태그와 내용을 다 포함한 전체 문자열, HTML문서의 기본 구성 단위|**<h1<k>>Hi</h1<k>>**|
|속성(attribute)|엘리먼트의 상세한 기능을 시작 태그 안에서 사용|<h1 **color**="blue">Hi</h1<k>>|
|속성값(value)|속성 값('' 또는 ""로 감쌈)|<h1 color=**"blue"**>Hi</h1<k>>|

```html
<!DOCTYPE html>

<html lang = "ko">

    <head>
        <meta charset="UTF-8">
        <title>문서 제목</title>
        <link rel="stylesheet" href="#">
        <style> /* CSS 적는 공간 */ </style>
        <script> // script 적는 공간(jQuery, JavaScript 등) </script>
    </head>

    <body>
        <!-- 여기 적힌 것들이 뷰포트에 나옴 -->
    </body>
</html>
```
- `<!DOCTYPE html>`
    - 
    문서 형식(document type) 선언: 브라우저에게 이 문서가 HTML5 문서임을 알림

- `<html>`
    - 
    `<html>` 요소: HTML 문서의 최상위 요소

- `<head>`
    - 
    `<head>` 요소: HTML 문서의 정보를 표현하는 요소들의 묶음
    - `<meta>` 
        : HTML 문서의 메타 데이터를 표현
        - HTML 문서의 문자 인코딩을 브라우저에게 알려주기 위해 사용하는데 기본 문자 인코딩은 UTF-8(제대로 명시)
    - `<title>`
        : HTML 문서의 제목<br>
        - 페이지를 방문자나 검색 엔진은 제목을 보고 내용을 예측해서 들어온다.
    - `<link>`
        : HTML 문서에 다른 파일 연결(외부 CSS파일 등)
    - `<style>`
        : HTML 문서에 스타일 시트 추가(CSS 적는 공간)
    - `<script>`
        : HTML 문서에 스크립트 추가

- `<body>`
    - 
    `<body>` 요소: 브라우저 화면(viewport)에 표시되는 요소들의 묶음


> ## 2. HTML의 태그