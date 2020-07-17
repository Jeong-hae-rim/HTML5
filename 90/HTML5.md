## 1. HTML5 개요

### 1) HTML5란

- HTML5는 웹 상에서 콘텐츠(content)를 구성하고 보여주기 위한 HTML 언어의 최신 표준 권고안
- HTML5는 HTML 4.01, XHTML 1.1 등을 대체하는 HTML의 차세대 표준
- HTML5는 XML이나 XHTML과는 달리 문법적으로 매우 유연하게 대처
- HTML5의 문법적 허용
  - 태그 이름에 대문자 사용
  - 속성값에 따옴표 생략
  - 속성값 생략
  - 빈 태그의 종료태그 (/) 생략

### 2) HTML5 문서의 기본 구조

- HTML5에서는 DOCTYPE의 선언이 매우 간단해졌다.

  ```html
  <!DOCTYPE html>
  ```

- 또한 문자셋(character set)의 선언도 매우 간단해짐

- HTML5에서의 기본 문자 인코딩(character encoding) 방식은 UTF-8

  - HTML5 이전

  ```html
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  ```

  - HTML5

  ```html
  <meta charset="UTF-8">
  ```

## 2. HTML5 변경사항

### 1) HTML5에서 추가된 요소 및 타입

#### 의미(sementic) 요소

- &lt;header&gt;, &lt;nav>, &lt;main>, &lt;section>, &lt;aside>, &lt;article>, &lt;footer>, &lt;figure>

#### 멀티미디어 요소

- &lt;video&gt;, &lt;audio&gt;

#### 그래픽 요소

- &lt;canvas&gt;, &lt;svg&gt;

#### input 요소의 타입

- number, date, time, calendar, range

### 2) HTML5에서 추가된 자바스크립트 API

- Geolocation
- Drag and Drop
- Web Storage
- Application Cache
- Web Worker
- Server Sent Events

### 3) HTML5에서 삭제된 기존 요소

| 삭제된 기존 요소 |         설명         |
| :--------------: | :------------------: |
|    <acronym>     |  <abbr> 태그로 대체  |
|     <applet>     | <object> 태그로 대체 |
|    <basefont>    |      CSS로 적용      |
|      <big>       |      CSS로 적용      |
|     <center>     |      CSS로 적용      |
|      <dir>       |   <ul> 태그로 대체   |
|      <font>      |      CSS로 적용      |
|     <frame>      |         삭제         |
|    <frameset>    |         삭제         |
|    <noframes>    |         삭제         |
|     <strike>     |      CSS로 적용      |
|       <tt>       |      CSS로 적용      |

### 4) 웹 브라우저의 HTML5 지원

- 현재 최신 버전의 주요 웹 브라우저들은 모두 HTML5를 지원

- 하지만 HTML5의 새로운 요소들이 구형 버전의 웹 브라우저에서는 제대로 표현되지 않을 수도 있다.

- 따라서 구형 버전의 웹 브라우저에 자신이 알지 못하는 새로운 HTML 요소를 다루는 방법을 알려주어야 한다.

- 다음 예제는 웹 브라우저가 알지 못하는 새로운 HTML 요소를 어떻게 다뤄야 하는지 알려주는 방법이다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Changes</title>
  	<script>document.createElement("newPara")</script>
  	<style>
  		newPara {
  			background-color: #F0F0F0;
  			display: block;
  			padding: 10px;
  			font-size: 14px;
  		} 
  	</style> 
  </head>
  <body>
  	<h1>새로운 HTML 요소의 정의</h1>
  	<h2>제목 2입니다.</h2>
  	<p>단락입니다.</p>
  	<newPara>우리 수업에서만 사용하는 단락입니다!</newPara>
  </body>
  </html>
  ```

  ![결과 1](https://user-images.githubusercontent.com/58800295/87220511-57e40880-c39f-11ea-952b-b510631192fb.png)

- 위와 같은 방법을 사용하면 모든 새로운 요소를 웹 브라우저에 설명할 수 있음
- 하지만 익스플로러 8과 그 이전 버전에서는 위와 같이 HTML 요소를 새롭게 정의하는 것을 허용하지 않음
- 이럴 때는 HTML Shiv 방법을 사용해야 함

### 5) HTML Shiv 방법

```html
<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->
```

- 위의 주석 코드를 &lt;head&gt; 태그 내에 삽입한다.

- 그러면 익스플로러 8과 그 이전 버전의 브라우저만이 이 자바스크립트 파일을 읽고 적용

- 이와 같은 방법으로 익스플로러 8과 그 이전 버전에서도 HTML5의 새로운 요소들을 자유롭게사용

  

```html
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<title>HTML5 Changes</title>
<!--[if lt IE 9]>
<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->
<style>
	header {
		background-color:lightgrey;
		height:100px;
	}
	nav {
		background-color:#339999;
		color:white;
		width:200px;
		height:300px;
		float:left;
	}
	section {
		width:200px;
		text-align:left;
		float:left;
		padding:10px;
	}
	footer {
		background-color:#FFCC00;
		height:100px;
		clear:both;
	}
	header, nav, section, footer { text-align:center; }
	header, footer { line-height:100px; }
	nav, section { line-height:240px; }
</style>
</head>
<body>
	<h1>HTML Shiv 방법</h1>
	<header>
		<h2>HEADER 영역</h2>
	</header>
	<nav>
		<h2>NAV 영역</h2>
	</nav>
	<section>
		<p>SECTION 영역</p>
	</section>
	<footer>
		<h2>FOOTER 영역</h2>
	</footer>
</body>
</html>
```

## 3.  HTML5 추가 요소

### 1) HTML5에서 추가된 의미(sementic)요소

|  의미 요소   |                             설명                             |
| :----------: | :----------------------------------------------------------: |
|   <header>   | HTML 문서나 섹션(section) 부분에 대한 헤더(header)를 정의함. |
|    <nav>     | HTML 문서 사이를 탐색할 수 있는 링크(link)의 집합을 정의함.  |
|    <main>    |          HTML 문서의 주요 콘텐츠(content)를 정의함.          |
|  <section>   |          HTML 문서에서 섹션(section) 부분을 정의함.          |
|  <article>   |  HTML 문서에서 독립적인 하나의 기사(article) 부분을 정의함.  |
|   <aside>    |  HTML 문서에서 페이지 부분 이외의 콘텐츠(content)를 정의함.  |
|   <figure>   | HTML 문서에서 그래픽과 비디오 등의 독립적인 콘텐츠(content)를 정의함. |
| <figcaption> |              figure 요소를 위한 캡션을 정의함.               |
|   <footer>   | HTML 문서나 섹션(section) 부분에 대한 푸터(footer)를 정의함. |
|    <bdi>     |  기본 출력방향과는 다른 방향으로 출력되는 텍스트를 정의함.   |
|    <mark>    |                하이라이팅된 텍스트를 정의함.                 |
|  <details>   |    사용자가 보거나 숨길 수 있는 추가적인 설명문을 정의함.    |
|  <summary>   |             details 요소에 나타날 내용을 정의함.             |
|   <dialog>   |    다이얼로그(dialog) 박스나 다이얼로그 윈도우를 정의함.     |
|  <menuitem>  | 사용자가 팝업 메뉴(popup menu)를 통해 선택할 수 있는 메뉴의 아이템(menu item)을 정의함. |
|   <meter>    |            정해진 범위 내의 스칼라 치수를 정의함.            |
|  <progress>  |               작업에 대한 진행 정도를 정의함.                |
|    <ruby>    |                  루비(ruby) 문자를 선언함.                   |
|     <rt>     |               본문 위에 나타날 문자를 정의함.                |
|     <rp>     | 루비(ruby) 문자를 지원하지 않는 브라우저에서만 나타날 내용을 정의함. |
|    <time>    |                    날짜와 시간을 정의함.                     |
|    <wbr>     | br 요소와는 달리 긴 단어가 화면의 맨 끝에 오면 상황에 따라 줄 바꿈 할 곳을 미리 정의함. |

### 2) HTML5에서 추가된 다양한 타입의 input 요소

| form 요소  |                             설명                             |
| :--------: | :----------------------------------------------------------: |
| <datalist> |     input 요소에 대해 미리 정의된 옵션 리스트를 명시함.      |
|  <keygen>  | form 요소 안에 두 개의 키(key)를 만들어주는 생성기를 명시함. |
|  <output>  |      스크립트 등으로 실행된 계산의 결과를 바로 나타냄.       |

### 3) HTML5에서 추가된 input 요소의 타입

#### 1.number

- &lt;input&gt; 태그의 type 속성값을 "number"로 설저하면 , input 요소는 사용자가 숫자를 입력할 수 있도록 해준다.

- number 타입이 일반 text 타입과 다른 점은 입력 필드 우측에 숫자의 크기를 조절할 수 있는 상하 버튼이 생기는 점

- 브라우저의 지원 여부에 따라 min 속성과 max 속성을 이용해 숫자 선택에 제한 값을 설정 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>number 타입을 이용한 숫자 입력</h1>
  	<form action="/examples/media/request.php">
  		여러분이 가장 좋아하는 숫자는 몇인가요?<br>
  		(단, 1부터 9까지에서 골라주세요!)<br><br>
  		<input type="number" name="favnum" min="1" max="9">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![결과2](https://user-images.githubusercontent.com/58800295/87221660-aa75f280-c3a8-11ea-8003-b6b719b56011.png)

#### 2. range(입력범위지정)

- &lt;input&gt; 태그의 type 속성 값을 "range"로 설정하면, input 요소는 사용자가 일정 범위 안의 값만을 입력할 수 있도록 해줌

- 브라우저 지원 여부에 따라 값을 선택하기 위한 수평 조절바를 보여준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>range 타입을 이용한 값의 입력</h1>
  	<form action="/examples/media/request.php">
  		여러분이 가장 좋아하는 숫자는 몇인가요?<br>
  		이번에는 수평바를 조절해서 골라주세요!<br><br>
  		0 <input type="range" name="favnum" min="1" max="9"> 9
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87222055-9384cf80-c3ab-11ea-9612-0e0f394cf83f.gif)

#### 3. color(색상입력)

- &lt;input&gt; 태그의 type 속성값을 "color"로 설정하면, input 요소는 사용자가 색상을 입력할 수 있도록 해준다.

- 선택된 색상은 #를 제외한 6자리 16진수 색상값으로 전송

- 브라우저 지원 여부에 따라 색상을 선택하기 위한 도구를 보여줌

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>color 타입을 이용한 색상 선택</h1>
  	<form action="/examples/media/request.php">
  		가장 좋아하는 색을 골라주세요 :<br><br>
  		<input type="color" name="favcolor" value="#CC6600">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87222154-73a1db80-c3ac-11ea-9bdb-8f10ac550ed4.gif)

#### 4. date (날짜입력)

- &lt;input&gt; 태그의 type 속성값을 "date"로 설정하면, input 요소는 사용자가 날짜를 입력할 수 있도록 해준다.
- 브라우저 지원 여부에 따라 날짜를 선택하기 위한 캘린더를 보여준다.

```html
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="UTF-8">
	<title>HTML5 Input Types</title>
</head>
<body>
	<h1>date 타입을 이용한 날짜 선택</h1>
	<form action="/examples/media/request.php">
		이 수업을 처음 들은 날을 기억하시나요?<br><br>
		<input type="date" name="startday">
		<input type="submit" value="전송">
	</form>
</body>
</html>
```

![Untitled1](https://user-images.githubusercontent.com/58800295/87222229-26723980-c3ad-11ea-9003-39f169ab2577.gif)

#### 5.time(시간 입력)

- &lt;input&gt; 태그의 type 속성값을 "time"으로 설정하면, input 요소는 사용자가 시간을 입력할 수 있도록 해준다.

- 브라우저 지원 여부에 따라 시간을 선택하기 위한 도구를 보여준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>time 타입을 이용한 시간 선택</h1>
  	<form action="/examples/media/request.php">
  		여러분이 태어난 시간은 몇 시인가요?<br><br>
  		<input type="time" name="birthtime">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87404650-63327080-c5f9-11ea-8be0-defde80be987.gif)

#### 6. datetime-local (날짜와 시간 입력)

- &lt;input&gt; 태그의 type 속성값을 "datetime-local"로 설정하면, input 요소는 날짜와 시간을 입력할 수 있도록 해준다.

- 브라우저 지원 여부에 따라 날짜를 선택하기 위한 캘린더와 시간을 선택하기 위한 도구를 보여준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>datetime-local 타입을 이용한 날짜와 시간 선택</h1>
  	<form action="/examples/media/request.php">
  		이 수업을 처음 들은 날을 골라주세요!<br>
  		그렇다면 혹시 그 시간도 기억하시나요?<br><br>
  		<input type="datetime-local" name="starttime">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87405563-96c1ca80-c5fa-11ea-90bd-9b00d0030480.gif)

#### 7. month(연도와 월 입력)

- &lt;input&gt; 태그의 type 속성값을 "month"로 설정하면, input 요소는 사용자가 연도와 월을 입력할 수 있게 해준다.

- 브라우저 지원 여부에 따라 연도와 월을 선택하기 위한 캘린더를 보여준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>month 타입을 이용한 연도와 월 선택</h1>
  	<form action="/examples/media/request.php">
  		여러분이 태어난 연월을 선택해 보세요!<br><br>
  		<input type="month" name="birthmonth">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87406682-01bfd100-c5fc-11ea-9236-985fe27f4708.gif)

#### 8. week(연도와 주 입력)

- &lt;input&gt; 태그의 type 속성값을 "week"로 설정하면, input 요소는 사용자가 연도와 몇 번째 주인지 입력할 수 있도록 해준다.

- 브라우저 지원 여부에 따라 연도와 주를 선택하기 위한 캘린더를 보여준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>week 타입을 이용한 연도와 주 선택</h1>
  	<form action="/examples/media/request.php">
  		오늘이 이번 달의 몇 번째 주인지 선택해주세요! <br>
  		<input type="week" name="nthweek">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87407394-0f298b00-c5fd-11ea-8bb5-e4f93718acc4.gif)

#### 9. email(이메일 입력)

- &lt;input&gt; 태그의 type 속성 값을 "email"로 설정하면, input 요소는 사용자가 email 주소를 입력할 수 있도록 해준다.

- 브라우저 지원 여부에 따라 전송할 때 입력한 email 주소가 유효한 email 주소인지 자동으로 검사해준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>email 타입을 이용한 email 주소 입력</h1>
  	<form action="/examples/media/request.php">
  		여러분의 이메일 주소를 입력해 주세요 :<br><br>
  		<input type="email" name="email">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87408045-e950b600-c5fd-11ea-8461-788677fcac42.gif)

#### 10. tel(전화번호 입력)

- &lt;input&gt; 태그의 type 속성값을 "tel"로 설정하면, input 요소는 사용자가 전화번호를 입력할 수있도록 해준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>tel 타입을 이용한 전화번호 입력</h1>
  	<form action="/examples/media/request.php">
  		여러분의 전화번호를 입력해 주세요 :<br><br>
  		<input type="tel" name="tel">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87408732-dee2ec00-c5fe-11ea-9fc0-c1cb94fff585.gif)

#### 11. url(URL 주소 입력)

- &lt;input&gt; 태그의 type 속성값을 "url"로 설정하면, input 요소는 사용자가 URL 주소를 입력할 수 있도록 해준다.

- 브라우저 지원 여부에 따라 전송할 때 입력한 URL 주소가 유효한 URL 주소인지 자동으로 검사한다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>url 타입을 이용한 URL 주소 입력</h1>
  	<form action="/examples/media/request.php">
  		TCPSchool의 URL 주소를 입력해 주세요 :<br><br>
  		<input type="url" name="url">
  		<input type="submit" value="전송"><br><br>
  		("http://"까지 모두 정확히 입력해야 전송할 수 있습니다.)
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87408459-7267ed00-c5fe-11ea-97df-393b718519b5.gif)

#### 12.  search(검색어 입력)

- &lt;input&gt; 태그의 type 속성값을 "search"로 설정하면, input 요소는 사용자가 검색어를 입력할 수 있도록 해준다.

- 이런 검색 필드는 보통 텍스트 필드(text field)와 동일하게 동작한다.

- search 타입이 일반 text 타입과 다른 점은 입력 필드에 검색어를 입력하면, 입력 필드 우측에 입력된 검색어를 바로 삭제할 수 있는 X 표시가 생긴다는 점이다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Input Types</title>
  </head>
  <body>
  	<h1>search 타입을 이용한 검색어 입력</h1>
  	<form action="/examples/media/request.php">
  		여러분이 평소에 가장 많이 찾아본 검색어를 입력해 주세요 :<br><br>
  		<input type="search" name="keyword">
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![Untitled1](https://user-images.githubusercontent.com/58800295/87409101-6f213100-c5ff-11ea-964c-adcd805d4d39.gif)

## 4. Input 요소의 속성

### 1) input 요소의 속성

- input 요소는 다양한 속성을 가질 수 있다.
- HTML에서 자주 사용되는 input 요소의 대표적인 속성
  1. value
  2. readonly
  3. disabled
  4. maxlength
  5. size

### 2)  HTML5 form 요소의 속성

- HTML5에서 새롭게 추가된 form 요소의 속성은 다음과 같다.
  1. autocomplete
  2. novalidate

### 3)  HTML5 input 요소의 속성

- HTML5에서 새롭게 추가된 input 요소의 속성은 다음과 같다.
  1. autocomplete

     - form 요소나 input 요소에 입력된 정보를 저장할지 안 할지를 명시

     - 이 속성의 속성 값이 on으로 설정되면 브라우저는 사용자가 입력하는 정보를 자동으로 저장

     - 이후에 입력되는 입력값을 저장된 정보를 바탕으로 자동 완성해준다.

     - **text, password, range, color, date, datetime-local, month, week, email, url, tel, search** 타입에만 쓸 수 있다.

       ```html
       <!DOCTYPE html>
       <html lang="ko">
       <head>
       	<meta charset="UTF-8">
       	<title>HTML5 Input Attributes</title>
       </head>
       <body>
       	<h1>autocomplete 속성을 이용한 자동 완성</h1>
       	<form action="/examples/media/request.php" autocomplete="on">
       		이름 : <input type="text" name="name"><br>
       		나이 : <input type="number" name="age" min="1" max="99" autocomplete="off"><br>
       		<br>
       		<a href="/html/intro">HTML 수업</a>
       		<p>input 요소에 데이터를 입력하고 전송 버튼을 누른 후에 F5키를 눌러 보세요!<br>
       		그리고 나서 같은 정보를 입력하려고 하면 이전 데이터가 아래에 팝업될 거에요!</p>
       		<input type="submit" value="전송">
       	</form>
       </body>
       </html>
       ```

       <img alt="autocomplete" src="https://user-images.githubusercontent.com/58800295/87521542-7dcf1d00-c6bf-11ea-9a48-fa63606533dc.png">

  2. novalidate

     - input 요소의 속성이 아닌 form 요소의 속성

     - 입력한 정보 (data)를 전송할 때 그 정보가 유효한지 아닌지를 검사하지 않았다는 것을 명시

     - url 타입이나 email 타입과 같이 자동으로 유효성 검사를 하는 input 타입에 이 속성을 사용하면 유효성 검사를 하지 않음

     - 이 속성이 사용된 form 요소로 전달받은 정보(data)는 반드시 서버 측에서 따로 유효성 검사를 해야 한다.

       ```html
       <!DOCTYPE html>
       <html lang="ko">
       <head>
       	<meta charset="UTF-8">
       	<title>HTML5 Input Attributes</title>
       </head>
       <body>
       	<h1>novalidate 속성을 이용한 유효성 검사 여부 명시</h1>
       	<form action="/examples/media/request.php">
       		여러분이 자주 들리는 사이트의 URL 주소를 입력해 주세요 :<br><br>
       		<input type="url" name="url">
       		<input type="submit" value="전송"><br>
       	</form>
       	<p><br>novalidate 속성을 적용하면 클라이언트 측의 유효성 검사를 건너뛸 수 있습니다.</p>
       	<form action="/examples/media/request.php" novalidate>
       		여러분이 자주 들리는 사이트의 URL 주소를 입력해 주세요 :<br><br>
       		<input type="url" name="url">
       		<input type="submit" value="전송">
       	</form>
       </body>
       </html>
       ```

       <img alt="novalidate" src="https://user-images.githubusercontent.com/58800295/87522204-4ad95900-c6c0-11ea-94b5-07d9028392b3.png">

  3. autofocus

     - 웹페이지가 로드(load)될 때, 속성이 적용된 input 요소에 자동으로 포커스(focus)가 가도록 해준다.

       ```html
       <!DOCTYPE html>
       <html lang="ko">
       <head>
       	<meta charset="UTF-8">
       	<title>HTML5 Input Attributes</title>
       </head>
       <body>
       	<h1>autofocus 속성을 이용한 오토 포커싱</h1>
       	<form action="/examples/media/request.php">
       		사용자 : <input type="text" name="username"><br>
       		비밀번호 : <input type="password" name="password" autofocus><br><br>
       		<input type="submit" value="전송">
       	</form>
       	<p>페이지 로드 시 자동으로 포커스가 비밀번호를 입력하는 input 요소에 가도록 합니다.</p>
       </body>
       </html>
       ```

       <img alt="autofocus" src="https://user-images.githubusercontent.com/58800295/87523391-d7d0e200-c6c1-11ea-8677-6a6d9e9f71ed.png">

  4. form

     - form 속성은 해당 input 요소의 위치에 상관 없이 포함될 form 요소를 명시
     - 포함할 form 요소의 id 속성값을 공백으로 연결해 둘 이상의 form 요소에 포함

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>form 속성</h1>
     	<form action="/examples/media/request.php" id="user">
     		사용자 : <input type="text" name="username"><br><br>
     		<input type="submit" value="전송">
     	</form>
     	<p>아래의 비밀번호를 입력하는 input 요소는 위치상으로는 form 요소에 포함되지 않습니다.<br>
     	하지만 form 속성을 이용하여 하나의 form으로 인식할 수 있습니다.
     	</p>
     	비밀번호 : <input type="password" name="password" form="user"><br>
     </body>
     </html>
     ```

     ![form](https://user-images.githubusercontent.com/58800295/87524133-c1775600-c6c2-11ea-897b-c3776418b604.png)

  5. formaction

     - 입력한 정보(data)를 전송할 때 정보가 전달될 서버 측 파일을 명시
     - 즉 formaction 속성은 form 요소의 action 속성을 덮어쓰게 됨
     - 이 속성을 사용하면 입력된 정보를 넘겨줄 서버 측 파일을 input 요소에서 바꿀 수 있게 됨
     - 이 속성은 submit, image 타입에서만 사용 가능

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>formaction 속성</h1>
     	<form action="/examples/media/request.php">
     		사용자 : <input type="text" name="username"><br>
     		비밀번호 : <input type="password" name="password"><br><br>
     		<input type="submit" value="전송">
     		<input type="submit" value="관리자 권한으로 전송"
     		formaction="/examples/media/request_admin.php"><br>
     	</form>
     </body>
     </html>
     ```

     ![formaction](https://user-images.githubusercontent.com/58800295/87524485-30ed4580-c6c3-11ea-9228-de429401510c.png)

  6. formenctype

     - 입력한 정보(data)를 전송할 때 암호화하는 방법을 명시
     - 즉 formenctype 속성은 form 요소의 enctype 속성을 덮어쓰게 됨
     - form 요소의 method 속성이 post일 때만 적용
     - 이 속성은 submit, image 타입에서만 사용할 수 있다.

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>formenctype 속성</h1>
     	<form action="/examples/media/request_enctype.php" method="post">
     		사용자 이름을 입력해주세요 : <input type="text" name="username"><br><br>
     		<input type="submit" value="암호화하여 전송" formenctype="multipart/form-data"><br>
     	</form>
     </body>
     </html>
     ```

     ![image](https://user-images.githubusercontent.com/58800295/87524875-b4a73200-c6c3-11ea-847d-f40c046d9d20.png)

     ![image](https://user-images.githubusercontent.com/58800295/87524916-c4bf1180-c6c3-11ea-8364-5f855e48ca03.png)

  7. formmethod

     - 입력한 정보(data)를 전송할 때 사용하는 http 메소드(method)를 명시
     - 즉 form 요소의 method 속성을 덮어쓰게 됨
     - 이 속성은 submit, image 타입에서만 사용 가능

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>formmethod 속성</h1>
     	<form action="/examples/media/request.php" method="get">
     		사용자 이름을 입력해주세요 : <input type="text" name="username"><br><br>
     		<input type="submit" value="post 방식으로 전송" formmethod="post"><br>
     	</form>
     </body>
     </html>
     ```

     ![image](https://user-images.githubusercontent.com/58800295/87525350-57f84700-c6c4-11ea-918b-92616fbb0093.png)

  8. formnovalidate

     - 입력한 정보(data)를 전송할 때 그 정보가 유효한지 아닌지 검사하지 않았다는 것을 명시
     - form 요소의 novalidate 속성을 덮어쓰게 된다.
     - 오직 submit 타입에서만 쓸 수 있다.

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>formnovalidate 속성</h1>
     	<form action="/examples/media/request.php">
     		여러분이 자주 들리는 사이트의 URL 주소를 입력해 주세요 : <input type="url" name="url">
     		<br><br>
     		<input type="submit" value="전송">
     		<input type="submit" value="novalidate 방식으로 전송" formnovalidate><br>
     	</form>
     </body>
     </html>
     ```

     <img alt="formnovalidate" src="https://user-images.githubusercontent.com/58800295/87525574-a60d4a80-c6c4-11ea-9f8b-5cc0ac9b98b9.png">

     - novalidate 방식으로 전송하기 버튼을 누르면 유효성 검사를 하지 않고 바로 서버로 전송한다.

  9. formtarget

     - 입력한 정보(data)를 전송한 후, 그 결과로 받은 응답 페이지를 어디에 출력할 것인지를 명시
     - form 요소의 target 속성을 덮어 쓴다.
     - 이 속성은 submit, image 타입에서만 사용할 수 있다.

     ```html
     <!DOCTYPE html>
     <html lang="ko">
     <head>
     	<meta charset="UTF-8">
     	<title>HTML5 Input Attributes</title>
     </head>
     <body>
     	<h1>formtarget 속성</h1>
     	<form action="/examples/media/request.php">
     		사용자 이름을 입력해주세요 : <input type="text" name="username"><br><br>
     		<input type="submit" value="전송">
     		<input type="submit" value="응답 화면을 새창에 표시" formtarget="_blank"><br>
     	</form>
     </body>
     </html>
     ```

     ![formtarget](https://user-images.githubusercontent.com/58800295/87525856-07351e00-c6c5-11ea-8ae8-f50770106fa5.png)

     - 전송 버튼을 누르면 새창에 띄우지 않고 그 창에서 그대로 실행이 되지만, 응답 화면을 새창에 표시 버튼을 누르면 새창이 뜨며 거기에 결과가 출력된다.

  10. height and width

      - &lt;input&gt; 태그의 type 속성이 "image"인 경우 height 속성과 width 속성을 사용해 이미지의 높이와 너비를 명시
      - 따라서  이 속성은 오로지 image 타입에서만 사용
      - 또한 이미지를 클릭하면 클릭한 곳의 x좌표와 y좌표가 x와 y라는 이름으로 같이 전송

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>height와 width 속성을 이용한 이미지의 크기 설정</h1>
      	<form action="/examples/media/request.php">
      		사용자 : <input type="text" name="username"><br>
      		비밀번호 : <input type="password" name="password" autofocus><br><br>
      		<input type="image" src="/examples/images/img_penguin.png" alt="전송" height="26" 
      		width="26">
      		그림을 클릭하시면 전송됩니다!
      	</form>
      </body>
      </html>
      ```

      ![image](https://user-images.githubusercontent.com/58800295/87526608-0486f880-c6c6-11ea-8716-4da3d33c3641.png)

      ![image](https://user-images.githubusercontent.com/58800295/87526830-444de000-c6c6-11ea-89d5-b932268aa744.png)

      - 자꾸 x와 y값이 바뀌던데 이유는 잘 모르겠다.

  11. list

      - 해당 input 요소에 대해 미리 정의된 옵션 리스트를 설정하는 datalist 요소와 관련
      - input 요소의 list 속성값이 datalist 요소의 id 속성값과 일치해야만 연결

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>list 속성을 이용한 datalist 요소</h1>
      	<form action="/examples/media/request.php">
      		<input list="lectures" name="lecture">
      			<datalist id="lectures">
      				<option value="HTML">
      				<option value="CSS">
      				<option value="JAVA">
      				<option value="C++">
      			</datalist>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      <img alt="datalist" src="https://user-images.githubusercontent.com/58800295/87527025-81b26d80-c6c6-11ea-9ce0-ce31085f68b5.png">

  12. min and max

      - input 요소에 입력할 수 있는 최솟값과 최댓값을 명시
      - **number, range, date, time, datetime-local, month, week** 타입에만 쓸 수 있다.

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>min과 max 속성을 이용한 입력값 제한</h1>
      	<form action="/examples/media/request.php">
      		여러분이 가장 좋아하는 숫자는 몇인가요?<br>
      		(단, 1부터 9까지에서 골라주세요!)<br><br>
      		<input type="number" name="favnum" min="1" max="9"><br><br>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      <img alt="제목 없음" src="https://user-images.githubusercontent.com/58800295/87527257-d229cb00-c6c6-11ea-85a9-702505fb9861.png">

  13. multiple

      - 사용자가 input 요소에 값을 두 개 이상 입력하는 것을 허용
      - email, file 타입에만 사용 가능

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>multiple 속성을 이용한 다중 파일 전송</h1>
      	<form action="/examples/media/request.php">
      		서버로 전송할 파일을 선택해주세요 :<br>
      		(여러 개의 파일 선택도 가능해요!)<br><br>
      		<input type="file" name="uploadfile" multiple><br><br>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      ![image](https://user-images.githubusercontent.com/58800295/87527483-259c1900-c6c7-11ea-9840-5973de625b50.png)

  14. pattern

      - input 요소에 입력된 값을 검사하기 위한 정규 표현식(regular expression)을 명시
      - 정규 표현식이란 문자열에서 특정한 규칙을 가지는 문자열의 집합을 찾아내기 위한 검색 패턴을 의미

      - **text, password, email, tel, url** 타입에서만 사용 가능

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>pattern 속성을 이용한 입력 형식 제한</h1>
      	<form action="/examples/media/request.php">
      		여러분의 이메일 주소를 입력해 주세요 :<br><br>
      		<input type="email" name="email"
      			pattern="[a-zA-Z0-9]+[@][a-zA-Z0-9]+[.]+[a-zA-Z]+[.]*[a-zA-Z]*" title="이메일 양식">
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      1. [a-zA-Z0-9] : 영문 소문자나 영문 대문자, 숫자 중 어느 것이라도 개수에 상관없이 나올 수 있음.

      2. [@] : '@' 문자만이 나와야 함.

      3. [.] : '.' 문자만이 나와야 함.

      4. [.]* : '.' 문자가 나와도 되고 나오지 않아도 됨.

      5. [a-zA-Z0-9]* : 영문 소문자나 영문 대문자, 숫자 중 어느 것이라도 개수에 상관없이 나와도 되고 나오지 않아도 됨.

      <img alt="제목 없음" src="https://user-images.githubusercontent.com/58800295/87527953-d30f2c80-c6c7-11ea-9d99-93b43f63a03e.png">

      <img alt="제목 없음" src="https://user-images.githubusercontent.com/58800295/87528021-ec17dd80-c6c7-11ea-8464-9a9f01455098.png">

  15. placeholder

      - input 요소에 입력되어야 할 값에 대한 힌트를 제공
      - 힌트는 예시가 될 수도 있고, 입력 형식에 대한 설명이 될 수도 있다.
      - placeholder 속성값은 해당 입력 필드에 포커스가 오게 되면 더 이상 표시되지 않는다.
      - text, password, email, tel, url, search 타입에서만 사용 가능하다.

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>placeholder 속성을 이용한 힌트 제공</h1>
      	<form action="/examples/media/request.php">
      		사용자 : <input type="text" name="username" placeholder="홍길동"><br>
      		비밀번호 : <input type="password" name="password" placeholder="1234"><br><br>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      ![image](https://user-images.githubusercontent.com/58800295/87528291-4d3fb100-c6c8-11ea-91fa-9a16d3392a34.png)

      ![image](https://user-images.githubusercontent.com/58800295/87528343-5fb9ea80-c6c8-11ea-9c24-41674ca479b4.png)

  16. required

      - 반드시 입력되어야 할 필수 input 요소를 명시
      - 이 속성이 설정된 모든 input 요소에 입력값이 존재해야만 서버로 전송(submit)할 수 있다.

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>required 속성을 이용한 필수 입력 설정</h1>
      	<form action="/examples/media/request.php">
      		이름 : <input type="text" name="name" required> (이름은 반드시 입력해야 해요!)<br>
      		나이 : <input type="number" name="age" min="1" max="99"><br><br>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      ![image](https://user-images.githubusercontent.com/58800295/87528528-9859c400-c6c8-11ea-82a0-5029370e2f7e.png)

      <img alt="제목 없음" src="https://user-images.githubusercontent.com/58800295/87528595-ae678480-c6c8-11ea-9ce3-9072892b3b8e.png">

  17. step

      - input 요소에 입력할 수 있도록 허용된 숫자 간격
      - 예를 들어 step 속성 값이 2이면, 입력이 허용되는 숫자는 ..., -4, -2, 0, 2, 4,... 가 된다.
      - number, range, date, time, datetime-local, month, week 타입에서만 사용할 수 있다.

      ```html
      <!DOCTYPE html>
      <html lang="ko">
      <head>
      	<meta charset="UTF-8">
      	<title>HTML5 Input Attributes</title>
      </head>
      <body>
      	<h1>step 속성을 이용한 입력 간격 설정</h1>
      	<form action="/examples/media/request.php">
      		여러분이 가장 좋아하는 숫자는 몇인가요?<br>
      		(단, -30부터 30사이에서 5단위로 골라주세요!)<br><br>
      		<input type="number" name="favnum" min="-30" max="30" step="5"><br><br>
      		<input type="submit" value="전송">
      	</form>
      </body>
      </html>
      ```

      <img alt="제목 없음" src="https://user-images.githubusercontent.com/58800295/87528800-00100f00-c6c9-11ea-832a-a1f9afe415f5.png">

## 5. HTML5 멀티미디어

### 1) 멀티미디어 파일 형식

#### 멀티미디어 파일 형식

- HTML5 이전까지는 웹 브라우저마다 어떤 종류의 멀티미디어 파일을 지원할지 각자 다른 방식으로 처리
- HTML5에서는 플래시와 같은 외부 플러그인의 도움 없이도 멀티미디어 파일을 간단히 사용
- 웹 브라우저는 파일의 타입(type)을 파일의 확장자로 판단
- 만약에 확장자가 .html인 파일을 보면, 웹 브라우저는 이 파일을 HTML 파일로써 다루게 될 것
- 비디오(video)나 사운드(sound)와 같은 멀티미디어 요소들은 멀티미디어 파일에 저장

#### 비디오(video) 파일 형식

- 대표적인 비디오 파일 형식

- HTML5 표준이 공식적으로 지원하는 비디오 파일 형식은 MP4, WebM, OGV

  | 파일 형식 | 파일 확장자 |                             설명                             |
  | :-------: | :---------: | :----------------------------------------------------------: |
  |   MPEG    | .mpg .mpeg  | Moving Picture Experts Group에 의해 개발되었으며, 변환 코덱을 이용하는 손실 압축 방식을 사용함. |
  |    MP4    |    .mp4     | Moving Picture Experts Group에 의해 개발되었으며, 적은 용량으로도 고품질의 영상 및 음성을 구현할 수 있어서 인터넷을 통한 스트리밍에 자주 활용됨. |
  |    OGV    |    .ogg     | Xiph 재단에 의해 개발되었으며, MP3의 대안으로 개발된 특허권으로 보호되지 않는 개방형 공개 멀티미디어 파일 형식임. |
  |   WebM    |    .webm    | 구글의 지원으로 개발된 개방형 공개 멀티미디어 파일 형식으로, 비디오 코덱으로는 VP8, 오디오 코덱으로는 Vorbis를 사용하는 멀티미디어 파일 형식임. |
  |    AVI    |    .avi     | Microsoft에 의해 개발되었으며, PC에서 동영상을 구현하기 위한 파일 형식임. |
  |    WMV    |    .wmv     | Microsoft에 의해 개발되었으며, Microsoft windows media player의 주 스트리밍 파일 형식임. |
  | QuickTime |    .mov     | Apple에 의해 개발되었으며, 매킨토시 컴퓨터에 동영상을 지원하기 위하여 개발된 파일 형식임. |
  | RealVideo |  .rm .ram   | Real Networks에 의해 개발되었으며, 스트리밍 기술을 이용한 동영상용 플러그 인 파일 형식임. |
  |   Flash   |  .swf .flv  | Macromedia에 의해 개발되었으며, 벡터 도형 처리 기반의 애니메이션 제작용 소프트웨어 파일 형식임. |

#### 오디오(audio) 파일 형식

- 대표적인 오디오 파일 형식

- HTML5 표준이 공식적으로 지원하는 오디오 파일 형식은 MP3, WAV, Ogg 

  | 파일 형식 | 파일 확장자 |                             설명                             |
  | :-------: | :---------: | :----------------------------------------------------------: |
  |    WAV    |    .wav     | IBM과 Microsoft에 의해 개발되었으며, 개인용 PC에서 오디오를 재생하기 위한 IBM과 Microsoft의 표준 오디오 파일 형식임. |
  |    Ogg    |    .ogg     | Xiph 재단에 의해 개발되었으며, MP3의 대안으로 개발된 특허권으로 보호되지 않는 개방형 공개 멀티미디어 파일 형식임. |
  |    MP3    |    .mp3     | Moving Picture Experts Group에 의해 개발되었으며, MPEG-1의 오디오 규격으로 개발된 손실 압축 파일 형식임. |
  |    MP4    |    .mp4     | Moving Picture Experts Group에 의해 개발되었으며, MPEG-4의 일부로 규정된 멀티미디어 컨테이너 파일 형식임. MP4는 비디오 파일 형식이기도 하지만 오디오에서도 사용할 수 있음. |
  |   MIDI    | .mid .midi  | 모든 전자 음악기기의 연주 정보를 상호 전달하기 위해 정해진 데이터 전송 규격임. |
  | RealAudio |  .rm .ram   | Real Networks에 의해 개발되었으며, 인터넷에서 실시간으로 음악을 들을 수 있는 스트리밍 사운드 기술임. |
  |    WMA    |    .wma     | Microsoft에 의해 개발되었으며, Microsoft windows media 기술에서 음악 정보(data)만을 압축하는 기술임. |
  |    AAC    |    .aac     | Apple에 의해 개발되었으며, iPhone, iPod, iTunes의 기본 오디오 파일 형식임. 표준적인 손실 압축 방식을 사용함. |



### 2) 비디오(video

#### 비디오(video) 요소

- HTML5 이전에는 웹 페이지에서 비디오(video)를 보여주기 위한 표준안이 없었음

- 비디오를 삽입하기 위해서는 플래시(flash)와 같은 외부 플러그인(plug-in)에 의존

- HTML5에서는 <video>태그를 이용하여 웹 페이지에 비디오를 삽입하는 표준화된 방식을 제공

- &lt;video&gt;태그를 지원하는 주요 웹 브라우저의 버전

  |    요소     | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :---------: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  | <video>태그 |                     9.0                     |                         4.0                         |                          3.5                          |                         4.0                         |                       10.5                        |

#### 비디오 요소의 속성

- control 속성 : 재생, 정지 및 소리의 조절 등 비디오의 기본적인 동작을 조절할 수 있는 패널을 생성. 또한 height와 width 속성을 이용하여 웹 브라우저에 삽입되는 비디오의 크기를 명시

- 웹 브라우저는 여러 개의 &lt;source&gt;태그 중 위쪽에서부터 순서대로 가장 먼저 인식되는 파일의 타입과 주소를 사용

- &lt;video&gt; 태그 사이에 존재하는 텍스트는 해당 웹 브라우저가 &lt;video&gt;태그를 지원하지 않을 때만 화면에 표시

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Video</title>
  </head>
  <body>
  	<h1>video 요소를 이용한 동영상 삽입</h1>
  	<video style="width:576px; height:360" controls>
  		<source src="/examples/media/sample_video_mp4.mp4" type="video/mp4">
  		<source src="/examples/media/sample_video_ogg.ogg" type="video/ogg">
  		이 문장은 사용자의 웹 브라우저가 video 요소를 지원하지 않을 때 나타납니다!
  	</video>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87744459-7fffbb80-c826-11ea-880d-06a4abb350a2.png)

- autoplay 속성 : 웹 페이지가 로드(load) 될 때 비디오를 자동으로 재생시켜 줄지 않을지를 설정

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Video</title>
  </head>
  <body>
  	<h1>autoplay 속성을 이용한 동영상의 자동 재생</h1>
  	<video width="576" height="360" controls autoplay>
  		<source src="/examples/media/sample_video_mp4.mp4" type="video/mp4">
  		<source src="/examples/media/sample_video_ogg.ogg" type="video/ogg">
  		이 문장은 사용자의 웹 브라우저가 video 요소를 지원하지 않을 때 나타납니다!
  	</video>
  </body>
  </html>
  ```

- loop 속성 : 비디오의 재생이 끝나도 계속적으로 반복해서 비디오를 재생

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Video</title>
  </head>
  <body>
  	<h1>loop 속성을 이용한 동영상의 반복 재생</h1>
  	<video width="576" height="360" controls loop>
  		<source src="/examples/media/sample_video_mp4.mp4" type="video/mp4">
  		<source src="/examples/media/sample_video_ogg.ogg" type="video/ogg">
  		이 문장은 사용자의 웹 브라우저가 video 요소를 지원하지 않을 때 나타납니다!
  	</video>
  </body>
  </html>
  ```

- &lt;track&gt; 태그는 비디오가 재생될 때 보일 자막이나 캡션 파일을 명시할 때 사용

- kind 속성 : 자막 문자열의 타입을 명시

- srclang 속성 : 해당 문자열의 언어 설정을 명시

- label 속성 : 사용자가 보게 될 라벨을 명시

  ```html
  <video style="width:576; height:360" controls>
      <source src="/examples/media/sample_video_mp4.mp4" type="video/mp4">
      <source src="/examples/media/sample_video_ogg.ogg" type="video/ogg">
      <track kind="subtitles" src="sample_subtitle_en.vtt" srclang="en" label="English">
      <track kind="subtitles" src="sample_subtitle_fr.vtt" srclang="fr" label="Francais">
      이 문장은 사용자의 웹 브라우저가 video 요소를 지원하지 않을 때 나타납니다!
  </video>
  ```

#### HTML5 비디오 파일 형식

- HTML5 표준이 공식적으로 지원하는 비디오 파일 형식은 MP4, WebM, OGV 

- MP4 

  - Moving Picture Experts Group에 의해 개발
  - 비디오 코덱으로는 H.268, 오디오 코덱으로는 ACC를 사용
  - 적은 용량으로도 고품질의 영상 및 음성을 구현할 수 있어 인터넷을 통한 스트리밍에 많이 활용되는 파일 형식

- WebM 

  - 구글의 지원으로 개발된 개방형 공개 멀티미디어 파일 형식
  - 비디오 코덱으로는 VP8, 오디오 코덱으로는 Vorbis를 사용

-  OGV 

  - Theora Ogg라고도 불림
  - Xiph 재단에 의해 MP3의 대안으로 개발된 특허권으로 보호되지 않는 개방형 공개 멀티미디어 파일 형식
  - 비디오 코덱으로는 Theora, 오디오 코덱으로는 Vorbis를 사용

- HTML5 비디오 파일 형식별 주요 웹 브라우저의 지원 여부

  | 파일 형식 | 미디어 타입 | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :-------: | :---------: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  |    MP4    |  video/mp4  |                      ○                      |                          ○                          |                           ○                           |                          ○                          |                         ○                         |
  |   WebM    | video/webm  |                      Χ                      |                          ○                          |                           ○                           |                          Χ                          |                         ○                         |
  |    OGV    |  video/ogg  |                      Χ                      |                          ○                          |                           ○                           |                          Χ                          |                         ○                         |

#### HTML5 video 요소

|  요소  |                             설명                             |
| :----: | :----------------------------------------------------------: |
| video  |            비디오와 영화 등 비디오 파일을 명시함.            |
| source | video 요소의 원본 파일에 대한 파일 형식 및 파일 주소를 여러 개 명시함.웹 브라우저는 위쪽에서부터 순서대로 가장 먼저 인식되는 파일 형식과 파일 주소를 사용함. |
| track  |         비디오 플레이어에 대한 텍스트 자막을 명시함.         |

#### HTML5 video 속성

|   속성   |                             설명                             |
| :------: | :----------------------------------------------------------: |
|   src    |                 비디오 파일의 경로를 명시함.                 |
|  height  |                 비디오 파일의 높이를 명시함.                 |
|  width   |                 비디오 파일의 너비를 명시함.                 |
| controls |    비디오의 기본적인 동작을 조절할 수 있는 패널를 명시함.    |
| autoplay |              비디오의 자동 재생 여부를 명시함.               |
|   loop   |              비디오의 반복 재생 여부를 명시함.               |
|  poster  | 비디오가 아직 준비 중일때 불러올 이미지 파일의 경로를 명시함. |
| preload  | 비디오를 재생하기 전에 파일의 내용을 모두 불러올지를 명시함. |



### 3) 오디오(audio)

#### 오디오(audio) 요소

- HTML5 이전에는 웹 페이지에서 오디오(audio)를 들려주기 위한 표준안이 없었음

- 따라서 비디오를 삽입하기 위해서는 플래시(flash)와 같은 외부 플러그인(plug-in)에 의존

- 하지만 HTML5에서는 &lt;audio&gt;태그를 이용하여 웹 페이지에 오디오를 삽입하는 표준화된 방식을 제공

- &lt;audio&gt; 태그를 지원하는 주요 웹 브라우저의 버전

  |    요소     | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :---------: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  | <audio>태그 |                     9.0                     |                         4.0                         |                          3.5                          |                         4.0                         |                       10.5                        |

#### 오디오 요소의 속성

- control 속성은 재생, 정지 및 소리의 조절 등 오디오의 기본적인 동작을 조절할 수 있는 패널을 생성

- 웹 브라우저는 여러 개의 &lt;source&gt;태그 중 위쪽에서부터 순서대로 가장 먼저 인식되는 파일의 타입과 주소를 사용

- &lt;audio&gt; 태그 사이에 존재하는 텍스트는 해당 웹 브라우저가 &lt;audio&gt;태그를 지원하지 않을 때만 화면에 표시

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Audio</title>
  </head>
  <body>
  	<h1>audio 요소를 이용한 소리 삽입</h1>
  	<audio controls>
  		<source src="/examples/media/sample_audio_ogg.ogg" type="audio/ogg">
  		<source src="/examples/media/sample_audio_mp3.mp3" type="audio/mp3">
  		이 문장은 사용자의 웹 브라우저가 audio 요소를 지원하지 않을 때 나타납니다!
  	</audio>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87746347-4b423300-c82b-11ea-98ba-ef4147f92f63.png)

- autoplay 속성 : 웹 페이지가 로드(load) 될 때 음악을 자동으로 재생시켜 줄지 않을지를 설정

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Audio</title>
  </head>
  <body>
  	<h1>autoplay 속성을 이용한 음악의 자동 재생</h1>
  	<audio controls autoplay>
  		<source src="/examples/media/sample_audio_ogg.ogg" type="audio/ogg">
  		<source src="/examples/media/sample_audio_mp3.mp3" type="audio/mp3">
  		이 문장은 사용자의 웹 브라우저가 audio 요소를 지원하지 않을 때 나타납니다!
  	</audio>
  </body>
  </html>
  ```

- loop 속성 : 설정하면 오디오의 재생이 끝나도 계속적으로 반복해서 오디오를 재생

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Audio</title>
  </head>
  <body>
  	<h1>loop 속성을 이용한 음악의 반복 재생</h1>
  	<audio controls loop>
  		<source src="/examples/media/sample_audio_ogg.ogg" type="audio/ogg">
  		<source src="/examples/media/sample_audio_mp3.mp3" type="audio/mp3">
  		이 문장은 사용자의 웹 브라우저가 audio 요소를 지원하지 않을 때 나타납니다!
  	</audio>
  </body>
  </html>
  ```

#### HTML5 오디오 파일 형식

- HTML5 표준이 공식적으로 지원하는 오디오 파일 형식은 MP3, WAV, Ogg

- MP3 

  - Moving Picture Experts Group에 의해 개발
  - MPEG-1의 오디오 규격으로 개발된 손실 압축형 파일 형식

- WAV 

  - IBM과 Microsoft에 의해 개발
  - 개인용 PC에서 오디오를 재생하기 위한 IBM과 Microsoft의 표준 오디오 파일 형식

- Ogg 

  - Xiph 재단에 의해 개발
  - MP3의 대안으로 개발된 특허권으로 보호되지 않는 개방형 공개 멀티미디어 파일 형식

- HTML5 오디오 파일 형식별 주요 웹 브라우저의 지원 여부

  | 파일 형식 | 미디어 타입 | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :-------: | :---------: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  |    MP3    |  audio/mp3  |                      ○                      |                          ○                          |                           ○                           |                          ○                          |                         ○                         |
  |    WAV    |  audio/wav  |                      Χ                      |                          ○                          |                           ○                           |                          ○                          |                         ○                         |
  |    Ogg    |  audio/ogg  |                      Χ                      |                          ○                          |                           ○                           |                          Χ                          |                         ○                         |

 #### HTML5 audio 요소

|  요소  |                             설명                             |
| :----: | :----------------------------------------------------------: |
| audio  |            오디오와 음악 등 오디오 파일을 명시함.            |
| source | audio 요소의 원본 파일에 대한 파일 형식 및 파일 주소를 여러 개 명시함.웹 브라우저는 위쪽에서부터 순서대로 가장 먼저 인식되는 파일 형식과 파일 주소를 사용함. |

 #### HTML5 audio 속성

|   속성   |                             설명                             |
| :------: | :----------------------------------------------------------: |
|   src    |                 오디오 파일의 경로를 명시함.                 |
| controls |    오디오의 기본적인 동작을 조절할 수 있는 패널를 명시함.    |
| autoplay |              오디오의 자동 재생 여부를 명시함.               |
|   loop   |              오디오의 반복 재생 여부를 명시함.               |
| preload  | 오디오를 재생하기 전에 파일의 내용을 모두 불러올지를 명시함. |



### 4)  플러그인(Plug-in)

#### 플러그인(Plug-in)

- HTML 플러그인이란 웹 브라우저의 표준 기능을 확장해 주는 프로그램을 의미
- 가장 널리 알려진 플러그인으로는 Java Applet, Flash Player, Pdf Reader 등이 있음
- 플러그인은 object 요소나 embed 요소를 사용하여 HTML 문서에 추가 가능

#### object 요소

- object 요소는 HTML 문서에 삽입할 객체(object)를 명시하는데 사용

- 이 요소는 모든 웹 브라우저에서 동작하며, 객체뿐만 아니라 또 다른 HTML 문서를 삽입 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Plugins</title>
  </head>
  <body>
  	<h1>object 요소를 이용한 pdf 파일 삽입</h1>
  	<object data="/examples/media/sample_plugins_pdf.pdf" style="width:100%; height:700px">
  	</object>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750224-d4f6fe00-c835-11ea-9efd-75d3baaa1926.png)

- object 요소는 이미지를 삽입할 때에도 사용 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Plugins</title>
  </head>
  <body>
  	<h1>object 요소를 이용한 image 파일 삽입</h1>
  	<object data="/examples/images/img_flower.png"></object>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750273-f5bf5380-c835-11ea-8b95-024ff52e4e6a.png)

#### embed 요소

- embed 요소는 HTML 문서에 삽입할 객체(object)를 명시하는데 사용

- embed 요소는 오래전부터 사용되어 왔지만, HTML5 이전까지는 HTML 표준이 아니었음

- 이 요소는 모든 웹 브라우저에서 동작하며, 객체뿐만 아니라 HTML 문서도 삽입 가능

- HTML5에서는 유효하지만, HTML4에서는 유효하지 않음

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Plugins</title>
  </head>
  <body>
  	<h1>embed 요소를 이용한 pdf 파일 삽입</h1>
  	<embed src="/examples/media/sample_plugins_pdf.pdf" style="width:100%; height:700px">
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750362-3323e100-c836-11ea-9df8-f5518ae44156.png)

- embed 요소는 이미지를 삽입할 때에도 사용 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Plugins</title>
  </head>
  <body>
  	<h1>embed 요소를 이용한 image 파일 삽입</h1>
  	<embed src="/examples/images/img_flower.jpg" style="width:350px; height:263px">
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750414-59498100-c836-11ea-9fcb-906f2065b11f.png)

## 6. HTML5 그래픽

### 1) Canvas

#### canvas 요소

- canvas 요소는 웹 페이지에 그래픽을 그려주는 쉽고 강력한 방법을 제공

- 이 요소는 그래픽을 위한 컨테이너(container) 역할만을 수행

- 따라서 실제로 그래픽을 그리기 위해서는 자바스크립트(JavaScript) 등의 스크립트 언어를 이용

- canvas 요소를 지원하는 주요 웹 브라우저의 버전

  |  요소  | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :----: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  | canvas |                     9.0                     |                         4.0                         |                          2.0                          |                         3.1                         |                        9.0                        |

#### canvas 요소의 속성

- canvas 요소는 테두리(border)도 콘텐츠(content)도 없는 웹 페이지 내의 단순한 사각형의 공간

- 그러므로 반드시 style 속성을 이용하여 캔버스의 크기를 설정

- canvas 요소를 스크립트(script)에서 접근하기 위해서는 해당 요소의 id 속성을 이용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 사각형 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  </body>
  </html>
  ```

  ![image-20200717140723084](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717140723084.png)

#### CSS 좌표 체계

- HTML 그래픽 요소에서 사용하는 x, y, z좌표는 다음 그림과 같은 좌표 체계를 따른다.

  ![CSS 좌표계](http://tcpschool.com/lectures/img_css_coordinate.png)

- CSS 좌표 체계에서 기준점은 브라우저의 왼쪽 상단

- 각 좌표축의 화살표 방향이 양의 방향이며, 반대쪽이 음의 방향

#### 사각형 그리기

- 캔버스를 정의한 후에는 스크립트를 이용하여 canvas 요소에 그래픽을 그릴 수 있다.

- 다음 예제는 스크립트를 이용하여 canvas 요소에 사각형을 그리는 예제이다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 사각형 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.strokeRect(10, 10, 250, 130);
  		
  		context.fillStyle = "rgba(255,0,0,1)";
  		context.fillRect(20, 20, 200, 100);
  		
  		context.clearRect(30, 30, 150, 50);
  	</script>
  	<p>
  		가장 바깥쪽에 strokeRect() 함수를 사용하여 선만으로 이루어진 사각형을 그립니다.<br>
  		그 다음에는 fillRect() 함수를 사용하여 빨간색으로 채워진 사각형을 그립니다.<br>
  		가장 안쪽에는 clearRect() 함수를 사용하여 사각형 모양으로 안의 내용을 지워줍니다.
  	</p>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750733-353a6f80-c837-11ea-915d-94143493bf0c.png)

- 위의 예제에서 사각형을 그리는 데 사용된 함수들은 다음 순서대로 인수를 전달받습니다.

  1. 사각형의 왼쪽 위 꼭짓점의 x좌표

  2. 사각형의 왼쪽 위 꼭짓점의 y좌표

  3. 사각형의 너비

  4. 사각형의 높이

- 사각형을 그리는데 사용하는 스크립트 함수

  |     함수     |                             설명                             |
  | :----------: | :----------------------------------------------------------: |
  | fillStyle()  | 사각형 영역을 채울 색상을 설정함. 색상값만을 사용할 수도 있고, 투명도까지 명시할 수 있음. |
  |  fillRect()  | 사각형을 그리기 시작할 시작점의 x, y좌표와 사각형의 너비, 높이 등을 설정함. |
  | strokeRect() |            사각형 영역에 테두리를 그릴 때 사용함.            |
  | clearRect()  |             지정된 사각형 영역을 투명하게 만듦.              |

#### 선 그리기

- 다음 예제는 스크립트를 이용하여 canvas 요소에 선을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 선 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.moveTo(0, 0);
  		context.lineTo(300, 100);
  		context.lineTo(150, 150);
  		context.stroke();
  	</script>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87750876-92cebc00-c837-11ea-97c7-749b1d47d844.png)

- 선을 그리는데 사용하는 스크립트 함수

  |   함수   | 설명                                                         |
  | :------: | :----------------------------------------------------------- |
  | moveTo() | 선이 시작될 좌표를 설정함.                                   |
  | lineTo() | 선이 끝나는 좌표를 설정함.<br />lineTo() 함수를 연속적으로 사용할 때의 시작 위치는 이전 선 그리기가 끝난 위치로 자동 설정됨. |
  | stroke() | 선 그리기 시작함.                                            |

- 이러한 선 그리기를 이용하면 도형을 만들 수도 있으며, 만든 도형에 색을 채우는 것도 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>선 그리기를 이용한 도형 만들기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.moveTo(0, 0);
  		context.lineTo(300, 200);
  		context.lineTo(150, 0);
  		context.lineTo(0, 0);
  		context.fillStyle = "#0099FF";
  		context.fill();
  		context.stroke();
  	</script>
  </body>
  </html>
  ```

  ![image-20200717141454332](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717141454332.png)

- 위의 예제에서는 우선 moveTo() 함수와 lineTo() 함수를 이용하여 선 그리기로 도형을 만든다.
- 그 후 fillStyle() 함수로 원하는 색상을 지정하고나서, fill() 함수를 사용하여 만든 도형에 색상을 칠한다.

#### 원 그리기

- 다음 예제는 스크립트를 이용하여 canvas 요소에 원을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 원 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.beginPath();
  		context.arc(150, 100, 50, 0, 2 * Math.PI);
  		context.stroke();
  	</script>
  </body>
  </html>
  ```

  ![image-20200717142414370](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717142414370.png)

- 위의 예제에서 사용된 arc() 함수는 다음 순서대로 인수를 전달받는다.

  1. 원의 중심 x좌표

  2. 원의 중심 y좌표

  3. 원의 반지름

  4. 원호를 그리기 시작할 각도

  5. 원호 그리기를 마칠 각도
     - Math.PI는 원의 원주를 지름으로 나눈 비율(원주율) 값으로 대략 3.14159를 나타낸다.

- 원을 그리는데 사용하는 스크립트 함수

  |    함수     | 설명                                                         |
  | :---------: | :----------------------------------------------------------- |
  | beginPath() | 도형 그리기를 시작함.                                        |
  |    arc()    | 원의 중심 좌표와 반지름, 원을 그리기 시작할 시작 위치와 종료 위치의 좌표, 그리는 방향 등을 설정함. |
  | closePath() | 도형 그리기를 마침.                                          |

- 이러한 원 그리기를 이용하면 원호 또한 간단히 만들 수 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>원 그리기를 이용한 원호 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.beginPath();
  		context.moveTo(100, 100);
  		context.arc(100, 100, 120, 0, 45 * Math.PI / 180);
  		context.closePath();
  		context.stroke();
  	</script>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87751637-72076600-c839-11ea-8f95-7c755ff7bfb7.png)

#### 텍스트(text) 그리기

- 다음 예제는 스크립트를 이용하여 canvas 요소에 텍스트를 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 텍스트 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  		context.font = "40px Arial";
  		context.fillText("CANVAS", 50, 90);
  		context.strokeText("HTML5", 80, 150);
  	</script>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87751698-99f6c980-c839-11ea-8d6c-09344478e317.png)

- 위의 예제에서 텍스트를 그리는 데 사용된 함수들은 다음 순서대로 인수를 전달받습니다.

  1. canvas 요소에 그릴 텍스트의 내용

  2. 텍스트의 왼쪽 위 꼭짓점의 x좌표

  3. 텍스트의 왼쪽 위 꼭짓점의 y좌표

- 텍스트를 그리는데 사용하는 스크립트 함수

  |     함수     | 설명                                                         |
  | :----------: | :----------------------------------------------------------- |
  |    font()    | 텍스트의 크기, 폰트(font)와 색상 등을 설정함.                |
  |  fillText()  | 텍스트의 내용과 텍스트를 그리기 시작할 시작 위치의 좌표를 설정함. |
  | strokeText() | 테두리만 있는 텍스트를 그릴 때 사용함.                       |

#### 그래디언트(gradient) 그리기

- 다음 예제는 스크립트를 이용하여 canvas 요소에 선형 그래디언트를 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 선형 그래디언트 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  
  		var gradient = context.createLinearGradient(0, 0, 200, 0);
  		gradient.addColorStop(0, "#FFCC00");
  		gradient.addColorStop(1, "#FFCCCC");
  
  		context.fillStyle = gradient;
  		context.font = "45px Arial black";
  		context.fillText("CANVAS", 15, 120);
  	</script>
  </body>
  </html>
  ```

  ![image-20200717142846907](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717142846907.png)

- 위의 예제에서 사용된 createLinearGradient() 함수는 다음 순서대로 인수를 전달받습니다.

  1. 선형 그래디언트가 시작하는 점의 x좌표

  2. 선형 그래디언트가 시작하는 점의 y좌표

  3. 선형 그래디언트가 끝나는 점의 x좌표

  4. 선형 그래디언트가 끝나는 점의 y좌표

- 이렇게 createLinearGradient() 함수를 사용하여 선형 그래디언트를 생성

- 이때 addColorStop() 함수를 사용하여 그래디언트에 사용될 색상을 명시

- 또한, 이렇게 생성된 그래디언트는 fillStyle이나 strokeStyle 속성을 이용하여 그리기 가능

- 다음 예제는 스크립트를 이용하여 canvas 요소에 원형 그래디언트를 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 원형 그래디언트 그리기</h1>
  	<canvas id="drawCanvas" width="300px" height="200px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<script>
  		var paper = document.getElementById("drawCanvas");
  		var context = paper.getContext("2d");
  
  		var gradient = context.createRadialGradient(100, 100, 200, 150, 150, 30);
  		gradient.addColorStop(0, "black");
  		gradient.addColorStop(1, "white");
  
  		context.fillStyle = gradient;
  		context.fillRect(0, 0, 300, 300);
  	</script>
  </body>
  </html>
  ```

  ![image-20200717143037208](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717143037208.png)

- 위의 예제에서 사용된 createRadialGradient() 함수는 다음 순서대로 인수를 전달받는다.

  1. 원형 그래디언트가 시작하는 원의 중심 x좌표

  2. 원형 그래디언트가 시작하는 원의 중심 y좌표

  3. 원형 그래디언트가 시작하는 원의 반지름

  4. 원형 그래디언트가 끝나는 원의 중심 x좌표

  5. 원형 그래디언트가 끝나는 원의 중심 y좌표

  6. 원형 그래디언트가 끝나는 원의 반지름

- 그래디언트(gradient)를 그리는데 사용하는 스크립트 함수

  - createLinearGradient() 함수와 createRadialGradient() 함수는 익스플로러 8과 그 이전 버전에서 지원 X

  |          함수          |                             설명                             |
  | :--------------------: | :----------------------------------------------------------: |
  | createLinearGradient() | 선형 그래디언트를 그리기 시작할 시작 위치와 종료 위치의 좌표를 설정함. |
  | createRadialGradient() | 원형 그래디언트를 그리기 시작할 큰 원의 중심 좌표, 반지름과 그래디언트가 끝날 작은 원의 중심 좌표, 반지름 등을 설정함. |
  |     addColorStop()     | 그래디언트의 색을 설정함. 시작점인 0에서부터 종료점인 1까지 다양한 색 지정이 가능함. |

#### 이미지 그리기

- 다음 예제는 스크립트를 이용하여 canvas 요소에 이미지를 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia Canvas</title>
  </head>
  <body>
  	<h1>canvas 요소에 이미지 그리기</h1>
  	<img id="Monalisa" src="/examples/images/img_monalisa.png" alt="모나리자" width="180" height="280">
  	<p>원본 이미지</p>
  	<canvas id="drawCanvas" width="200px" height="300px" style="border: 1px solid #993300">
  		이 문장은 사용자의 웹 브라우저가 canvas 요소를 지원하지 않을 때 나타납니다!
  	</canvas>
  	<p><button onclick="drawImage()">이미지 그리기</button></p>
  	<script>
  		function drawImage() {
  			var paper = document.getElementById("drawCanvas");
  			var context = paper.getContext("2d");
  			var srcImg = document.getElementById("Monalisa");
  			context.drawImage(srcImg, 10, 10);
  		}
  	</script>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87752036-5ea8ca80-c83a-11ea-9b8d-79d137321a75.png)

- 위의 예제에서 사용된 drawImage() 함수는 다음 순서대로 인수를 전달받는다.

  1. canvas 요소에 그릴 이미지의 주소

  2. 이미지의 왼쪽 위 꼭짓점의 x좌표

  3. 이미지의 왼쪽 위 꼭짓점의 y좌표

- 이미지를 그리는데 사용하는 스크립트 함수

|    함수     |                             설명                             |
| :---------: | :----------------------------------------------------------: |
| drawImage() | canvas 요소에 그릴 이미지의 주소와 이미지가 그려질 시작 위치를 설정함 |

### 2) SVG

#### svg 요소

- svg 요소는 Scalable Vector Graphics를 의미

- XML 기반의 W3C 그래픽 표준 권고안

- 기존에 사용해 왔던 canvas 요소로는 벡터(vector) 이미지를 표현할 수 없었음

- 하지만 svg 요소는 픽셀 기반인 웹 페이지에서 픽셀의 영향을 받지 않는 벡터 이미지를 표현

- 따라서 이 요소는 도표나 그래프 등 벡터 기반의 다이어그램(diagram)를 표현하는 데 매우 효과적

- svg 요소를 지원하는 주요 웹 브라우저의 버전

  | 요소 | ![ie](http://tcpschool.com/img/icon-ie.png) | ![chrome](http://tcpschool.com/img/icon-chrome.png) | ![firefox](http://tcpschool.com/img/icon-firefox.png) | ![safari](http://tcpschool.com/img/icon-safari.png) | ![opera](http://tcpschool.com/img/icon-opera.png) |
  | :--: | :-----------------------------------------: | :-------------------------------------------------: | :---------------------------------------------------: | :-------------------------------------------------: | :-----------------------------------------------: |
  | svg  |                     9.0                     |                         4.0                         |                          3.0                          |                         3.2                         |                       10.1                        |

#### 사각형 그리기

- 다음 예제는 rect 요소를 사용하여 사각형을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 사각형 그리기</h1>
  	<svg width="200" height="150">
  		<rect width="200" height="150" stroke="orange" stroke-width="5" fill="yellow"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87752268-ebec1f00-c83a-11ea-83a0-a247f9462fbb.png)

- 사각형을 그리는데 사용하는 rect 요소의 속성

  |     속성     |             설명             |
  | :----------: | :--------------------------: |
  |    width     |    도형의 너비를 설정함.     |
  |    height    |    도형의 높이를 설정함.     |
  |    stroke    | 도형의 테두리 색상을 설정함. |
  | stroke-width | 도형의 테두리 굵기를 설정함. |
  |     fill     |  도형을 채울 색상을 설정함.  |
  |   opacity    |   도형의 투명도를 설정함.    |

- 다음 예제와 같이 style 속성을 사용하여 한 번에 설정

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 사각형 그리기</h1>
  	<svg width="200" height="150">
  		<rect width="200" height="150" style="stroke:orange; stroke-width:5; fill:yellow; opacity:1;"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image-20200717143817067](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717143817067.png)

- rect 요소에 x, y, rx, ry 속성을 추가하여 모서리가 둥근 사각형을 그릴 수도 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 모서리가 둥근 사각형 그리기</h1>
  	<svg width="250" height="200">
  		<rect width="200" height="150" x="20" y="20" rx="20" ry="20" stroke="orange" stroke-width="5" fill="yellow"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87752417-45544e00-c83b-11ea-9329-7b82e10381bb.png)

- 모서리가 둥근 사각형을 그리는데 사용하는 rect 요소의 속성

  | 속성 |                   설명                    |
  | :--: | :---------------------------------------: |
  |  x   | 사각형의 왼쪽 위 꼭짓점의 x좌표를 설정함. |
  |  y   | 사각형의 왼쪽 위 꼭짓점의 y좌표를 설정함. |
  |  rx  | 사각형 모서리 굴곡의 x축 반지름을 설정함. |
  |  ry  | 사각형 모서리 굴곡의 y축 반지름을 설정함. |

#### 선 그리기

- 다음 예제는 line 요소를 사용하여 선을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 선 그리기</h1>
  	<svg width="250" height="200">
  		<line x1="50" y1="50" x2="200" y2="150" stroke="orange" stroke-width="5"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87752474-6e74de80-c83b-11ea-80d6-9862cb33425d.png)

- 선을 그리는데 사용하는 line 요소의 속성

  | 속성 |                설명                |
  | :--: | :--------------------------------: |
  |  x1  | 선이 시작될 위치의 x좌표를 설정함. |
  |  y1  | 선이 시작될 위치의 y좌표를 설정함. |
  |  x2  | 선이 끝나는 위치의 x좌표를 설정함. |
  |  y2  | 선이 끝나는 위치의 y좌표를 설정함. |

####  원 그리기

- 다음 예제는 circle 요소를 사용하여 원을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 원 그리기</h1>
  	<svg width="300" height="300">
  		<circle cx="150" cy="120" r="100" stroke="orange" stroke-width="5" fill="yellow"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image-20200717144135190](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200717144135190.png)

- 원을 그리는데 사용하는 circle 요소의 속성

  | 속성 |           설명            |
  | :--: | :-----------------------: |
  |  cx  | 원의 중심 x좌표를 설정함. |
  |  cy  | 원의 중심 y좌표를 설정함. |
  |  r   |   원의 반지름을 설정함.   |

#### 타원 그리기

- 다음 예제는 ellipse 요소를 사용하여 타원을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 타원 그리기</h1>
  	<svg width="300" height="300">
  		<ellipse cx="150" cy="100" rx="120" ry="70" stroke="orange" stroke-width="5" fill="yellow"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87755425-f1993300-c841-11ea-8184-fea6cade7b9d.png)

- 타원을 그리는데 사용하는 ellipse 요소의 속성

  | 속성 |            설명             |
  | :--: | :-------------------------: |
  |  cx  | 타원 중심의 x좌표를 설정함. |
  |  cy  | 타원 중심의 y좌표를 설정함. |
  |  rx  | 타원의 x축 반지름을 설정함. |
  |  ry  | 타원의 y축 반지름을 설정함. |

#### 다각형 그리기

- 다음 예제는 polygon 요소를 사용하여 별모양의 다각형을 그리는 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML5 Multimedia SVG</title>
  </head>
  <body>
  	<h1>svg 요소를 이용한 다각형 그리기</h1>
  	<svg width="300" height="300">
  		<polygon points="10,100 190,100 30,200 100,40 170,200"
  			stroke="orange" stroke-width="5" fill="yellow"/>
  		이 문장은 사용자의 웹 브라우저가 svg 요소를 지원하지 않을 때 나타납니다!
  	</svg>
  </body>
  </html>
  ```

  ![image](https://user-images.githubusercontent.com/58800295/87755596-3ae98280-c842-11ea-9b10-87b19a3a357b.png)

- 다각형을 그리는데 사용하는 polygon 요소의 속성

  |  속성  |                       설명                        |
  | :----: | :-----------------------------------------------: |
  | points | 다각형의 각 꼭짓점이 표시될 위치의 좌표를 설정함. |

- points 속성은 다각형을 이루는 각 꼭짓점의 x좌표와 y좌표를 명시
- 이때 첫 번째 꼭짓점부터 시작하여 마지막 꼭짓점까지 차례대로 선으로 연결되어 다각형을 표현

### 3) Canvas vs SVG

- canvas 요소와 svg 요소는 거의 같은 결과물을 얻을 수 있는 비슷한 동작을 하는 요소
- 어떤 경우에는 canvas 요소를 사용하는 것이 더 나으며, 어떤 경우에는 svg 요소를 사용하는 것이 더 나은 경우가 있다.

#### 작업 환경에 따른 선택의 기준

- 다음 그림은 화면 크기 및 픽셀 수에 따른 렌더링 시간(rendering time)을 보여줌

- 렌더링(Rendering)

  - 프로그램을 사용하여 모델로부터 영상이나 화면을 만들어내는 과정을 가리킴
  - 렌더링 시간이란 코드를 실행하여 그 결과가 화면에 표시되는 시간을 의미

  ![image](https://user-images.githubusercontent.com/58800295/87755962-fe6a5680-c842-11ea-9f94-fa1b354e1565.png)

- Canvas 요소의 성능은 화면이 작거나, 픽셀 수가 많을 경우(>10K)에 좋다.
- SVG 요소의 성능은 화면이 크거나, 픽셀 수가 적을 경우(<10K)에 좋다.
- 따라서 각 작업 환경에 맞는 그래픽 요소를 선택하여 사용하는 것이 가장 좋다.

#### 작업 종류에 따른 선택의 기준

- 다음 그림은 canvas 요소와 svg 요소를 사용할 때 선택의 기준을 제시

  ![canvas와 svg 사이의 선택 기준](http://tcpschool.com/lectures/img_html5_canvas_svg.png)

- Canvas 요소는 복잡하고 고성능의 애니메이션(animation) 작업이나 동영상 조작 등의 작업에 잘 어울리낟.
- SVG 요소는 고품질의 문서 작업이나 정적 이미지의 조작 작업 등에 잘 어울린다.
- 따라서 각 작업 종류에 맞는 그래픽 요소를 선택하여 사용하는 것이 가장 좋다.

#### Canvas와 SVG의 차이점

|                   Canvas                    |                           SVG                           |
| :-----------------------------------------: | :-----------------------------------------------------: |
|              픽셀(pixel) 기반               |                    모양(shape) 기반                     |
|               단일 HTML 요소                |          DOM의 일부분이 되는 다중 그래픽 요소           |
| 스크립트(script)를 통해서만 수정할 수 있음. |   스크립트(script) 및 CSS를 통해서도 수정할 수 있음.    |
|      그래픽이 주작업인 게임에 적합함.       | 렌더링 영역이 넓은 응용 프로그램(application)에 적합함. |