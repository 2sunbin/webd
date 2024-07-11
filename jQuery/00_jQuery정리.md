# 📃 jQuery

<details>
<summary>목차</summary>

[1. jQuery이란 무엇일까요?](#1-jquery이란-무엇일까요)

[1-1. jQuery 사용 방법](#1-1-jquery-사용-방법)

</details>

<br><br><br><hr><hr>

> # 1. jQuery이란 무엇일까요?
- JavaScript 프로그램을 작성하면서 자주 사용하는 기능들의 집합인 라이브러리

<br><hr>

>> ## 1-1. jQuery 사용 방법
- 다운로드(https://jquery.com/) 후 서버에 업로드하고, HTML 문서에 추가
```HTML
<head>
    <!-- 다운 받은 위치의 jquery 집어넣기  -->
    <script src="jquery-3.7.1.min.js"></script>
    <script>
        // script 작업
    </script>
</head>
```

- CDN 활용
```HTML
<head>
    <!-- 다운 안 해도 CDN 적어 넣으면 사용 가능  -->
    <!-- 현재 상태는 버전을 따로 설정 안 해줘도 사람들이 많이 사용하는 버전으로 알아서 설정해줌 -->
    <script src="https://code.jquery.com/jquery.min.js"></script>
    <!-- 
        특정 버전을 선택해서 적으려면 
        https://code.jquery.com/jquery-3.7.1.min.js
        이런식으로 버전을 직접 적어주면 됨
    -->
    <script>
        // script 작업
    </script>
</head>
```