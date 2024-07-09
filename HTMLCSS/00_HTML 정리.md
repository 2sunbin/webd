# 📃 HTML

<details>
<summary>목차</summary>

[1. HTML이란 무엇일까요?](#1-html이란-무엇일까요)

- [1-1. HTML의 기본 구성](#1-1-html의-기본-구성)


[2. HTML의 태그](#2-html의-태그)

- [2-1. 글자 태그](#2-1-글자-태그)
- [2-2. 목록 태그](#2-2-목록-태그)
- [2-3. 표 태그](#2-3-표-태그)


</details>

<br>

---
---

> ## 1. HTML이란 무엇일까요?
HTML(Hyper-Text Markup Language)

- 웹 브라우저에 표시되도록 설계된 문서의 표준 마크업 언어
    ##### 마크업 언어 : 태그 등을 이용해 문서나 데이터의 구조를 명시하기 위한 규칙을 정리한 언어

<br>

>> ### 1-1. HTML의 기본 구성

|요소|의미|예시|
|-|-|-|
|태그(tag)|'<>'로 둘러싸인 문자열로 시작태그(<>)와 종료태그(</>)로 구성|**<h1<k>></h1<k>>**|
|내용(content)|태그로 둘러싸인 문자열|<h1<k>>**Hi**</h1<k>>|
|요소(element)|태그와 내용을 다 포함한 전체 문자열, HTML문서의 기본 구성 단위|**<h1<k>>Hi</h1<k>>**|
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
- `<!DOCTYPE html>` : 문서 형식(document type) 선언: 브라우저에게 이 문서가 HTML5 문서임을 알림

- `<html>` 요소: HTML 문서의 최상위 요소

- `<head>` 요소: HTML 문서의 정보를 표현하는 요소들의 묶음
    - `<meta>` 
        : HTML 문서의 메타 데이터를 표현
        - HTML 문서의 문자 인코딩을 브라우저에게 알려주기 위해 사용하는데 기본 문자 인코딩은 UTF-8(제대로 명시)
    - `<title>`
        : HTML 문서의 제목<br>
        - 페이지를 방문자나 검색 엔진은 제목을 보고 내용을 예측해서 들어옴
    - `<link>`
        : HTML 문서에 다른 파일 연결(외부 CSS파일 등)
    - `<style>`
        : HTML 문서에 스타일 시트 추가(CSS 적는 공간)
    - `<script>`
        : HTML 문서에 스크립트 추가

- `<body>` 요소: 브라우저 화면(viewport)에 표시되는 요소들의 묶음

<br><br><br>
---

> ## 2. HTML의 태그

- '<>'로 둘러싸인 문자열로 시작태그(<>)와 종료태그(</>)로 구성

<br>

>> ### 2-1. 글자 태그
- HTML 문서에서 가장 큰 비중을 차지

|종류|태그|
|-|-|
|제목|`<h1>~<h6>`|
|본문|`<p>, <br>, <hr>`|
|앵커|`<a>`|
|글자 형태|`<b>, <strong>, <i>, <em>, <small>, <mark>, <sub>, <sup> 등`|

- 제목
    - `<hn>` : 제목(headings)

        `<h1> ~ <h6>` 까지 있으며 `<h1>`이 제일 크고 `<h6>`이 제일 작음
        - 페이지에서 특별한 제목이 되는거라 `<h1>`은 가능하면 가장 크고 중요한 한 번만 부분에 걸어주는 게 좋음 (다른 것들은 여러번 나와도 됨)
        ```HTML
        <h1>Hello</h1>
        ```

- 본문
    - `<p>` : 단락(paragraph)
        블럭 레벨(후에 더 자세한 설명)
        ```HTML
        <p>
            Hello World
        </p>
        ```
        

    - `<br>` : 내부 텍스트의 강제 개행(break)
        ```HTML
        <p>
            Hello<br>
            World
        </p>
        ```


    - `<hr>` : 가로 구분선(horizontal break)
        ```HTML
        <hr>
        <h1>Hello</h1>
        ```
        
- 앵커
    - `<a>` : 외부 연결(hyper-link)
    - 서로 다른 HTML 문서 사이를 이동하거나 HTML 문서 내부에서 특정한 위치로 이동할 때 사용
        - href 속성: 외부 연결 URL(원격 참조 URL; hyper-reference) 설정
        ```HTML
        <!-- 문서 외부로 이동 -->
        <a href="https://www.naver.com">네이버</a>

        <!-- 문서 내부에서 이동 -->
        <a href="#">문서의 상단으로 이동</a>
        <a href="#here">id 속성이 "here"인 요소로 이동</a>
        ```

- 글자 형태
    - `<b>` : 의미 없이 내용을 진하게 표시
    - `<strong>` : 중요하고 긴급한 내용을 강조, 웹 페이지의 내용 중 강조하고 싶은 부분이 있을 때 사용
    - `<i>` : 의미 없이 기울임 꼴로 표시
    - `<em>` : 내용의 강조를 위해 기울임 꼴로 표시
    - `<small>` : 기본 글자보다 작은 text로 지정
    - `<mark>` : highlighted text로 지정
    - `<sub>` : 기본 글자보다 아래에 쓰인 텍스트로 지정
    - `<sup>` : 기본 글자보다 위에 쓰인 텍스트로 지정

<br>

>> ### 2-2. 목록 태그
- 비슷한 것들끼리 묶어서 사용

|태그|의미|설명|
|-|-|-|
|`<ul>`|unordered list|순서가 없는 목록|
|`<ol>`|ordered list|순서가 있는 목록|
|`<li>`|list item|목록 요소|
|`<dl>`|definition list|정의 목록|
|`<dt>`|definition term|정의 용어|
|`<dd>`|definition description|정의 설명|

##### `<ul>`요소나 `<ol>`요소에는 `<li>`요소만 들어갈 수 있음
##### `<dl>`요소에는 `<dt>`요소와 `<dd>`요소만 들어갈 수 있음

- `<ul>` : 순서가 없는 목록(unordered list)
    
    ```HTML
    <ul>
        <li>HTML</li>
        <li>CSS</li>
    </ul>
    ```

- `<ol>` : 순서가 있는 목록(ordered list)
    
    ```HTML
    <ol>
        <li>HTML</li>
        <li>CSS</li>
    </ol>
    ```

- 중첩된 목록: 목록 안에 목록이 들어가는 형태
    
    ```HTML
    <ul>
        <li>HTML
            <!-- 안쪽 목록은 반드시 <li>요소 안에 들어가야 함 -->
            <ul>
                <li>HTML Tutorial</li>
                <li>HTML Elements</li>
            </ul>
        </li>
        <li>CSS
            <ul>
                <li>CSS Tutorial</li>
                <li>CSS blocks</li>
            </ul>
        </li>
    </ul>
    ```

- `<dl>` : 정의 목록(definition list)
    
    ```HTML
    <!-- 정의 목록 -->
    <dl>
        <!-- 정의 용어 -->
        <dt>HTML</dt>

        <!-- 용어 설명 -->
        <dd>HTML stands for Hyper Text Markup Language</dd>
        <dd>HTML describes the structure of a Web page</dd>
    </dl>
    ```
#### 예제: 01_list.html    

<br>

>> ### 2-3. 표 태그

|태그|의미|설명|
|-|-|-|
|`<table>`||표(Table)를 작성하기 위한 기본 태그|
|`<thead>`|table header|표의 제목 행들의 묶음(생략 가능)|
|`<tbody>`|table body|표의 본문 행들의 묶음(생략 불가능)|
|`<tfoot>`|table footer|표의 푸터 행들의 묶음(생략 가능)|
|`<tr>`|table row|표의 행(row) 표현|
|`<th>`|table header|표의 제목 셀을 표현|
|`<td>`|table data|표의 본문 셀을 표현|

##### 표는 HTML 문서에서 구조가 가장 복잡한 콘텐츠라 반드시 필요한 경우에만 사용
#### 예제: 02_table.html