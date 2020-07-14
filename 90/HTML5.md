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
  2. autofocus
  3. form
  4. formaction
  5. formenctype
  6. formmethod
  7. formnovalidate
  8. formtarget
  9. height and width
  10. list
  11. min and max
  12. multiple
  13. pattern
  14. placeholder
  15. required
  16. step
  17. 