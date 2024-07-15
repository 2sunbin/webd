# 📃 jQuery

<details>
<summary>목차</summary>

[1. jQuery이란 무엇일까요?](#1-jquery이란-무엇일까요)

- [1-1. jQuery 사용 방법](#1-1-jquery-사용-방법)
- [1-2. jQuery 기본 코드](#1-2-jquery-기본-코드)
- [1-3. jQuery 함수](#1-3-jquery-함수)

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
<br><hr>

>> ## 1-2. jQuery 기본 코드
- window 객체의 load 이벤트와 비슷한 이벤트로 DOM 트리를 완성한 시점에서 발생하게끔 적음

```javascript
<script>
    // 첫 번째 방법
    jQuery(docuemnt).ready(funtion(){
        // 코드 작성
    });
    // 첫 번째 방법
    $(document).ready(function(){
        // 코드 작성
    });
    // 세 번째 방법. 다 같은 의미라 가장 간단한 세 번째 방법을 많이 쓰긴 함
    $(function(){
        // 코드 작성
    });
</script>
```

<br><hr>

>> ## 1-3. jQuery 함수

- jQuery 객체를 포함해서 반환(인자: 객체)

```javascript
    $(document).height();
```

- document 객체의 ready 이벤트 핸들러 등록(인자: 함수)
 
 ```javascript
    $(funtion() {
        $('body').html('Hi');
    });
 ```

- DOM에서 HTML 요소를 탐색 후 HTMLElement 객체를 포함하는 jQuery 객체 생성 후 반환(인자: 선택자 형태의 문자열)
 
 ```javascript
    $('#test').css('color', 'blue');
 ```

 - 주어진 HTML 마크업으로 새로운 HTMLElement 객체 생성 후 그 객체를 포함하는 jQuery 객체를 생성해서 반환(인자: HTML 마크업 형태의 문자열)

 ```javascript
    $('<span>NEW</span>').appendTo('.new');
 ```

>> ## 1-4. jQuery 선택자

- jQuery 함수로 DOM에서 특정 객체를 탐색하기 위한 방법
- CSS 선택자를 그대로 사용 가능
- jQuery 라이브러리에서 추가한 선택자도 있음

```HTML
    <script>
        // $기호가 단독으로 쓰이면 jQuery 함수 별칭
        $('#test').css('color', 'blue');

        // JavaScript 에서는 아래와 같이 쓰임 -->
        // document.querySelector('#test').style.color = 'blue';
    </script>
```

- 태그 선택자

    ```HTML
        <p>HI</p>
        <script>
            $('p').css('color', 'blue');
        </script>
    ```

- 아이디 선택자

    ```HTML
        <p id='hi'>HI</p>
        <script>
            $('#hi').css('color', 'blue');
        </script>
    ```

- 클래스 선택자

    ```HTML
        <p class='hi'>HI</p>
        <p class='hi'>HEllo</p>
        <script>
            $('.hi').css('color', 'blue');
            <!-- jQuery 객체의 메서드들은 jQuery 객체에 담겨 있는 HTMLElement 객체가 몇 개인지에 상관없이 메서드 내부에서 반복문으로 순차적으로 조작(자바스크립트러처럼 for문 필요 없음) -->
        </script>
    ```

- 자식 선택자

    ```HTML
        <ul>
            <li>Red</li>
            <li>Blue<span>Gray<span></li>
        </ul>
        <script>
            <!-- 자식 선택자 -->
            $('ul > li').css('color', 'red');
            <!-- 후손 선택자 -->
            $('ul span').css('font-weight', 'bold');
        </script>
    ```