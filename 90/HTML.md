# HTML

## HTML 시작

### 1) HTML 개요

- HTML은 **웹 페이지를 만드는 데에 사용하는 언어**이다.
- **모든 태그는 이미 정의**되어 있고, 각각의 태그와 속성을 사용하기만 하면 된다.



### 2) HTML 기초

- HTML이란?

  - HyperText Markup Language의 약자이다.

    - HyperText : 하이퍼텍스트를 가장 중요한 특징으로 하는
    - Markup : 마크업이라는 형식을 가진
    - Language : 컴퓨터 프로그래밍 언어

  - 웹 페이지는 HTML 문서라고도 불리고, HTML 태그들로 구성된다.

  - 각각의 HTML 태그는 **웹 페이지의 디자인이나 기능을 결정**하는 데 사용된다.

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    
    <head>
    	<meta charset="UTF-8">
    </head>
    
    <body>
    
    	<h1>Hello, World!</h1>
    	<h2>2020년 7월 7일</h2>
    	<h3>구공팩토리 2일차</h3>
    	<p>HTML과 CSS를 정리하시라고 하셨다.</p>
    	<p>2주 안에 끝내는 게 베스트!</p>
    
    </body>
    
    </html>
    ```

    ![result1](https://user-images.githubusercontent.com/58800295/87107718-795bcc00-c29b-11ea-812a-0932d8adcf61.png)

- HTML 태그(tag)

  - 태그 이름을 **꺽쇠 괄호(<>)로 감싸서 표현**한다.

  - 문법

    ```html
    1. <태그이름> //시작 태그
    2. </태그이름> //종료 태그
    ```

    ```
    <h1>오늘의 명언</h1> //heading1, 줄바꿈을 하자는 약속을 암묵적으로함
    우리 모두는 <strong>자신의 힘</strong>으로 발견한 내용을 가장 쉽게 익힌다. (도널드 커누스)
    ```

    <img alt="result2" src="https://user-images.githubusercontent.com/58800295/87107834-c344b200-c29b-11ea-98e3-594217fd3929.PNG">

  - HTML 태그는 보통 **시작 태그**(start tag, opening tag)와 **종료 태그**(end tag, closing tag) 한 쌍으로 구성된다.

  - 종료 태그는 시작 태그와 전부 똑같지만 앞에 슬래시(/)가 존재한다.

  - 태그에 따라 시작 태그만 있고 종료 태그는 없는 태그도 존재한다.

    이것을 **빈 태그**(Empty tag)라고 한다.

    ```html
    <img><br><hr> //이런 태그 같이 종료 태그 없이 시작 태그만을 가지는 태그
    ```

- HTML 작성

  - HTML 문서는 **윈도우의 메모장, 리눅스의 vi와 같은 기본 에디터로도 작성**할 수 있다.
  - HTML 문서의 작성을 마친 후 확장자를 **.html**로 저장하면 웹 브라우저에서 바로 확인할 수 있다.



### 3) HTML 기본 구조

다음은 HTML 문서의 기본적인 구조를 보여주는 그림이다.

<img alt="structure" src="https://user-images.githubusercontent.com/58800295/87107868-d6578200-c29b-11ea-876f-a74e5443485e.PNG">

- ```html
  <!DOCTYPE html> <!-- 현재 문서가 HTML5문서임을 명시한다. -->
  <html> <!-- HTML 문서의 루트(root) 요소를 정의한다. -->
      <head> 
          <!-- HTML 문서의 메타데이터 *(metadata)를 정의한다. -->
          <!-- 본문이 아닌 태그들은 head 태그 안에 들어온다. -->
          <title>HTML 문서의 제목</title>
          <!-- HTML 문서의 제목을 정의한다. -->
      </head>
      <body> 
          <!-- 웹 브라우저를 통해 보이는 내용(content, 본문) 부분이다. -->
          <!-- 본문인 태그들은 전부 body 태그 안에 들어간다. -->
          <h1>제목 크기 1</h1>
          <h2>제목 크기 2</h2>
          <!-- h1~h6까지 있으며 제목(heading)을 나타낸다. -->
          <p>단락 부분</p>
          <!-- 단락(paragraph)을 나타낸다. -->
      </body>
  </html>
  ```

- 메타데이터(metadata) 

  - HTML 문서에 대한 정보(data)로, 웹 브라우저에는 **직접적으로 표현되지 않는 정보**를 의미

  - ```html
    <title>, <style>, <meta>, <link>, <Script>, <base> 태그 등을 이용하여 표현
    ```

- 타이틀(title)

  - 웹 브라우저의 **툴바(toolbar)에 표시**된다.
  - 웹 브라우저의 즐겨찾기(favorites)에 추가할 때 **즐겨찾기의 제목**이 된다.
  - 검색 엔진의 결과 페이지에 **제목으로 표시**된다.



### 4) HTML 요소 구조

- HTML 요소 구조

  - HTML ***요소(element)**는 **여러 속성**을 가질 수 있다.

  - 이러한 ***속성(attribute)**은 **해당 요소에 대한 추가적인 정보를 제공**한다.

  - HTML 요소는 시작 태그로 시작해서 종료 태그로 끝난다.

    <img alt="structure2" src="https://user-images.githubusercontent.com/58800295/87107883-e2dbda80-c29b-11ea-888d-9c7beba03bcf.PNG">

  - 속성은 HTML 요소 중에서도 **언제나 시작 태그 내에서만 정의**된다.

  - **속성 명 = 속성 값(value)**로 표현된다.

    ```
    <태그이름 속성이름="속성값">
    ```

  - 속성 명에 따라 **그 기능이 약속**되어 있다.
  - 속성의 **순서는 상관 없다.** 
  - 태그 자체의 **빈약한 기능에 다양한 기능들을 추가**할 수 있다.

- 속성 이름은 소문자로

  - HTML5 표준에서는 속성 이름에 대소문자를 구별하지 않는다.
  - 하지만 **될 수 있으면 소문자로 작성**하는 걸 권장
  - XHTML에서는 속성 이름을 더욱 엄격하게 소문자로만 사용

- 속성 값은 **언제나 따옴표**로 감싼다

  - HTML5 표준에서는 속성값에 따옴표 사용을 강제하지 않는다.

  - 하지만 속성값을 따옴표로 감싸지 않으면, 예상치 못한 오류가 발생할 수도 있다.

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    
    <head>
    	<meta charset="UTF-8">
    	<title>HTML Tag Structure</title>
    </head>
    
    <body>
    
    	<h1>속성값의 따옴표</h1>
    	<p>속성값에 정말로 따옴표가 필요한가?</p>
    	<img src="quotes.jpg" alt="이미지가 없어요"><br>
    	<img src="quotes.jpg" alt=이미지가 없어요>
        <!-- <img> 태그의 alt 속성은 이미지를 불러올 수 없는 상황에서 이미지 대신--> 
        <!-- 보이는 문자열을 설정할 수 있다. -->
    	
    </body>
    
    </html>
    ```

    <img alt="result3" src="https://user-images.githubusercontent.com/58800295/87107913-eff8c980-c29b-11ea-9d90-11f41504a676.PNG">

  - 위 예제처럼 속성 값에 띄어쓰기가 들어가게 되면 반드시 따옴표를 사용해야 정확한 값을 지정할 수 있다.

  - 속성 값을 감쌀 때는 **보통 큰따옴표("")가 사용**되며, 작은 따옴표('')도 사용할 수 있다.

## HTML 텍스트 요소

### 1) 제목

- HTML은 제목을 표현할 수 있는 **다양한 크기의 <h> 태그**를 제공한다.

- 가장 큰 **<h1> 태그부터 <h6> 태그까지** 다양한 크기로 제목을 표현할 수 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Headings</title>
  </head>
  
  <body>
  
  	<h1>제목1의 크기입니다!</h1>
  	<h2>제목2의 크기입니다!</h2>
  	<h3>제목3의 크기입니다!</h3>
  	<h4>제목4의 크기입니다!</h4>
  	<h5>제목5의 크기입니다!</h5>
  	<h6>제목6의 크기입니다!</h6>
  
  </body>
  
  </html>
  ```

  <img alt="result4" src="https://user-images.githubusercontent.com/58800295/87107951-0dc62e80-c29c-11ea-9e10-a347980e39c8.PNG">

- h 태그는 제목의 표현이라는 기능 외에도 또 다른 중요한 역할을 한다.
  - 여러 검색 엔진들이 **h 태그를 이용해 키워드를 수집하고 내용을 파악**
  - HTML 문서에 포함되는 제목은 h 태그로 작성해야만 검색 엔진에 의해 제대로 검색될 확률을 높임
- 종료 태그
  - 대부분 웹 브라우저는 종료 태그를 사용하지 않아도 HTML 문서를 잘 표현해준다.
  - 그러나 **종료 태그가 없으면 예상치 못한 오류나 결과가 발생**할 수 있다.
  - XHTML이나 XML 같은 문법이 엄격한 언어에서는 종료 태그의 유무를 엄격하게 검사
  - 가급적 종료 태그를 빠뜨리지 않고 코드를 작성해야 한다.



### 2) 단락

#### 단락(paragragh)

- 내용상 끊어서 구분할 수 있는 하나하나의 부분을 의미하며, 문단이라고도 부른다.
- HTML에서는 **<p> 태그**를 이용해 이런 단락을 표현한다.
- 태그 위아래로는 **약간의 여백(margin)**이 자동으로 삽입된다.

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Paragraph</title>
</head>

<body>

	<h1>제목1의 크기입니다!</h1>
	<h2>제목2의 크기입니다!</h2>
	<h3>제목3의 크기입니다!</h3>
	<p>여기서부터 단락입니다.</p>

</body>

</html>
```

<img alt="result5" src="https://user-images.githubusercontent.com/58800295/87107986-220a2b80-c29c-11ea-9406-e9af2d64e365.PNG">

#### 띄어쓰기와 줄 나누기

- HTML 코드에서는 띄어쓰기와 줄 나누기를 여러 번 하더라도 웹 브라우저 화면 상에는 전혀 영향을 주지 못한다.

- 웹 브라우저는 여러 번 띄어쓰고 줄 나누기를 해도 **오직 하나의 띄어쓰기와 줄로만 인식**한다.

- ```
  <br>태그(break line)을 사용하면 새로운 단락을 만들지 않고도 줄을 나눌 수 있다.
  이러한 태그는 종료 태그가 없으므로 빈 태그(empty tag)이다.
  ```

#### 텍스트(text) 서식 미리 정의하기

- HTML 코드에서 작성한 텍스트 서식을 그대로 표현하려면 **<pre>태그**를 사용한다.

- 태그(preformatted text) 내에 작성된 텍스트의 모든 띄어쓰기와 줄 나누기는 웹 브라우저에 그대로 표현된다.
  
<pre> 태그 내에 작성된 텍스트의 글꼴(font)은 **고정폭 글꼴(fixed-width font)**로 자동변환된다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Paragraph</title>
  </head>
  
  <body>
  
  	<pre>
  줄을 나누고 싶어서
  이렇게 줄을 나눠봤습니다.
  
  과연     그대로     출력이     될까요?
  	</pre>
  
  </body>
  
  </html>
  ```

  <img alt="result6" src="https://user-images.githubusercontent.com/58800295/87108022-3e0dcd00-c29c-11ea-8a8b-fae73647a136.PNG">

#### 수평 가로 구분선

- 단락을 나눌 때나 내용상의 구분을 표현하고자 할 때 사용한다.

- 이렇게 사용되는 수평 가로 구분선을 HTML 코드에서는 **<hr> 태그**(horizontal rule)로 만든다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Paragraph</title>
  </head>
  
  <body>
  
  	<p>저는 하나의 단락입니다.</p>
  	<hr>
  	<p>저는 하나의 단락입니다.</p>
  	<hr>
  	<p>저는 하나의 단락입니다.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result7" src="https://user-images.githubusercontent.com/58800295/87108049-4cf47f80-c29c-11ea-93a1-30cdbde72f28.PNG">



### 3) 서식

#### 강조 효과

- 텍스트를 굵게 표현하고 싶을 때 **<b>태그(bold text)나 <strong>태그**를 사용한다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>b태그와 strong태그의 차이점</h1>
  	<p><b>"이 부분"</b>은 단순히 글씨가 굵은 부분이에요!</p>
  	<p><strong>"이 부분"</strong>은 중요한 부분이라서 굵게 표현됐어요!</p>
  
  </body>
  
  </html>
  ```

  <img alt="result8" src="https://user-images.githubusercontent.com/58800295/87108095-6990b780-c29c-11ea-9327-473ad250d2f5.PNG">

- <b> 태그는 **단순히 화면의 텍스트를 굵게 표현**해준다.

  하지만 <strong> 태그는 텍스트를 굵게 표현해줄 뿐 아니라 **그 내용이 중요하다는 의미**도 함께 담고 있다.

- <i> 태그와 <em> 태그는 **이탤릭체를 표현**해준다.

  <em> 태그 또한 이탤릭체로 표현해줄 뿐 아니라 **그 내용이 중요하다는 의미**도 담고 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>i태그와 em태그의 차이점</h1>
  	<p><i>"이 부분"</i>은 단순히 글씨가 이탤릭체인 부분이에요!</p>
  	<p><em>"이 부분"</em>은 중요한 부분이라서 이탤릭체로 표현됐어요!</p>
  	
  </body>
  
  </html>
  ```

  <img alt="result9" src="https://user-images.githubusercontent.com/58800295/87108133-7d3c1e00-c29c-11ea-897b-1e84627754bd.PNG">

- 검색 엔진은 **<strong>태그와 <em>태그를 사용하여 강조된 텍스트를 더 중요하게 인식**한다.

#### 하이라이팅 효과

- <mark> 태그는 **텍스트에 하이라이팅 효과를 적용**시켜준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>mark태그를 이용한 하이라이팅</h1>
  	<p><mark>"이 부분"</mark>만 하이라이팅하고 싶어요.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result10" src="https://user-images.githubusercontent.com/58800295/87108146-862cef80-c29c-11ea-9e77-0c9a73883016.PNG">

#### 삭제 효과

- <del>태그(delete)는 **텍스트 중앙에 가로줄을 만들어 텍스트를 지운 것 같은 효과**를 내준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>del태그를 이용한 삭제 효과</h1>
  	<p><del>"이 부분"</del>을 지운 것처럼 하고 싶어요.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result11" src="https://user-images.githubusercontent.com/58800295/87108187-a492eb00-c29c-11ea-99ef-b31b837b5e53.PNG">

#### 삽입 효과

- <ins>태그(insert)는 **텍스트 밑에 가로줄을 만들어 빈칸에 텍스트를 삽입한 효과**를 내준다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>ins태그를 이용한 삽입 효과</h1>
  	<p><ins>"밑줄 친 부분"</ins>에 들어갈 알맞은 말을 고르세요.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result12" src="https://user-images.githubusercontent.com/58800295/87108206-af4d8000-c29c-11ea-856d-cc9840da666b.PNG">

#### 위첨자와 아래첨자 효과

- 위첨자는 **<sup>태그(superscript)**를 사용하며, 아래첨자는 **<sub>태그(subscirpt)**를 사용하여 표현

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Formatting</title>
  </head>
  
  <body>
  
  	<h1>sup태그와 sub태그를 이용한 첨자</h1>
  	<p>X<sup>2</sup> + Y<sup>3</sup> = Z</p>
  	<p>물을 나타내는 화학식은 H<sub>2</sub>O 입니다.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result13" src="https://user-images.githubusercontent.com/58800295/87108219-b96f7e80-c29c-11ea-9a7a-cf6098c0764f.PNG">



### 4) 인용구

#### 짧은 인용구

- 짧은 인용구는 **<q>태그(quotation)를 사용하여 표현**하며, 자동으로 앞뒤에 큰따옴표가 붙는다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Quotations</title>
  </head>
  
  <body>
  
  	<h1>q태그를 이용한 짧은 인용구</h1>
  	<p>HTML의 정의는
  	<q>웹 페이지를 만들기 위한 하이퍼텍스트 마크업 언어</q>
  	입니다.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result14" src="https://user-images.githubusercontent.com/58800295/87108231-c7250400-c29c-11ea-8f3b-419c62d79ef2.PNG">

#### 블록 인용구

- 길이가 긴 인용문의 경우 **<blockquote>태그(block quatation)를 사용**하여 표현

- 인용 부분을 별도의 단락으로 구분하여 나타냄

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Quotations</title>
  </head>
  
  <body>
  
  	<h1>blockquote태그를 이용한 블록 인용구</h1>
  	<p>HTML의 정의</p>
  	<blockquote>
  	인터넷 서비스의 하나인 월드 와이드 웹을 통해 볼 수 있는 문서를 만들 때 사용하는 프로그래밍 언어의 한 종류이다.
  	</blockquote>
  
  </body>
  
  </html>
  ```

  <img alt="result15" src="https://user-images.githubusercontent.com/58800295/87108247-d1470280-c29c-11ea-8a91-451bb84d4d35.PNG">

#### 축약형 표현

- 용어의 축약형을 표현하기 위해 **<abbr>태그(abbrevitation)**를 사용한다.

- <abbr>태그 위에 마우스를 위치하면 title 속성에 명시한 용어의 원형이 나온다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Quotations</title>
  </head>
  
  <body>
  
  	<h1>abbr태그를 이용한 축약형 표현</h1>
  	<p>아래의 단락에서 HTML5이라는 단어 위에 마우스를 올려놓아 보세요!</p>
  	<p><strong><abbr title="HyperText Markup Language 5">HTML5</abbr></strong>
  	란 웹 문서를 제작하는 데 쓰이는 프로그래밍 언어인 HTML의 최신규격입니다.</p>
  
  </body>
  
  </html>
  ```

  ![result16](https://user-images.githubusercontent.com/58800295/87108267-dc9a2e00-c29c-11ea-9f2c-9785fbb75292.png)

#### 주소표현

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Quotations</title>
</head>

<body>

	<h1>address태그를 이용한 주소의 표현</h1>
	<address>
		서울특별시<br> 
		강남구 테헤란로
	</address>

</body>

</html>
```

- address 태그를 사용하여 주소를 표현한다.

- 주소는 이탤릭체로 표현되며 위 아래로 약간의 공백이 자동으로 삽입된다.

  <img alt="result17" src="https://user-images.githubusercontent.com/58800295/87108288-e885f000-c29c-11ea-8749-47348bd9a01f.PNG">



### 5) 주석

#### 주석

- 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미

- 주석은 다른 HTML 코드와 달리 웹 브라우저에 의해 표현되지 않음

- HTML에서 주석을 표현하는 방법은 다음과 같다.

- ```html
  <!-- 주석내용 -->
  ```

- 주석의 시작태그(<!--)에는 느낌표가 있지만 종료 태그(-->)에는 느낌표가 없다.

- 주석은 코드의 어느 부분에서라도 사용할 수 있다.

- 여러 줄에 걸쳐 주석을 작성해도 정확히 인식한다.

#### 중첩 주석

- **HTML 주석 안에 또 다른 주석을 작성할 수는 없다.**

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Comments</title>
  </head>
  
  <body>
  
  	<h1>HTML 중첩 주석</h1>
  	<p>이 부분은 조금 어려운 코드입니다.</p>
  	<!-- 
  		<!-- 주석 안에 또 다른 주석을 삽입했습니다. -->
  		위와 같이 어려운 코드의 이해를 돕기 위해서 개발자가 적어놓은 설명입니다.
  	-->
  
  </body>
  
  </html>
  ```

  <img alt="result18" src="https://user-images.githubusercontent.com/58800295/87108304-f2a7ee80-c29c-11ea-8f5d-2439a89d2006.PNG">

- 위의 예제처럼 HTML 주석 안에 또 다른 주석을 삽입할 시 삽입한 주석의 종료 태그를 첫 번째 주석이 자신의 종료 태그로 인식

- 따라서 삽입한 주석의 종료 태그 다음부터 첫 번째 주석의 종료 태그까지 모든 내용이 그대로 웹 페이지에 노출됨



### 6) 엔티티

- HTML에 미리 예약된 몇몇 문자를 **HTML 예약어**라고 부른다.
- 이런 예약어를 HTML 코드에서 사용하면, 웹 브라우저는 그것을 평소와는 다른 의미로 해석
- 따라서 HTML 예약어를 **기존에 사용하던 의미 그대로 사용하기 위해 별도로 만든 문자셋**이 엔티티(entity)

#### 엔티티 형태

```html
&엔티티이름;
&#엔티티숫자;
```

- 코드 내에서 꺽쇠 괄호를 사용했을 시

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Entities</title>
  </head>
  
  <body>
  
  	<h1>HTML 엔티티</h1>
  	<p><p>태그는 단락을 나타내는 태그입니다.</p>
  	<p>&lt;p&gt;태그는 단락을 나타내는 태그입니다.</p>
  
  </body>
  
  </html>
  ```

  <img alt="result19" src="https://user-images.githubusercontent.com/58800295/87108319-fe93b080-c29c-11ea-8dda-1d8f00df5672.PNG">

- 위처럼 HTML 코드에서 사용된 꺽쇠괄호(<>)는 HTML 태그의 시작과 끝의 의미로 해석됨

#### 대표적인 엔티티

| 엔티티 문자 | 엔티티 이름 | 16진수 엔티티 숫자 |       설명        |
| :---------: | :---------: | :----------------: | :---------------: |
|             |   & nbsp;   |      &# 160;       | 줄 바꿈 없는 공백 |
|      <      |    & lt;    |       &# 60;       |     보다 작은     |
|      >      |    & gt;    |       &# 62;       |      보다 큰      |
|      &      |   & amp;    |       & #38;       |     AND 기호      |
|      "      |   & quot;   |       & #34;       |     큰따옴표      |
|      '      |   & apos;   |       &# 39;       |    작은따옴표     |

#### 발음 구별 부호

- 발음을 나타내는 부호는 악센트

- 악센트는 단독으로 사용하지 않으며, 다른 문자와 함께 사용

- 정확하게 표현하기 위해 이 부호를 별도로 제공

  | 발음 구별 부호 | 문자 | 16진수 엔티티 | 결과 |
  | :------------: | :--: | :-----------: | :--: |
  |        ̀        |  a   |   a&# 768;    |  à   |
  |        ́        |  a   |   a&# 769;    |  á   |
  |        ̂        |  a   |   a&# 770;    |  â   |
  |        ̃        |  a   |   a&# 771;    |  ã   |
  |        ̀        |  O   |   O&# 768;    |  Ò   |
  |        ́        |  O   |   O&# 769;    |  Ó   |
  |        ̂        |  O   |   O&# 770;    |  Ô   |
  |        ̃        |  O   |   O&# 771;    |  Õ   |

#### 심볼 특수문자

- HTML 예약어 이외에도 키보드에 입력할 수 없는 문자를 표현하기 위해 심볼 특수 문자를 사용

- 심볼 특수문자에는 수학 용어, 그리스 문자, 국제 통화 등이 있다.

  | 심볼 특수문자 | 엔티티 이름 | 16진수 엔티티 |   설명   |
  | :-----------: | :---------: | :-----------: | :------: |
  |       ¢       |   & cent;   |    &# 162;    |   센트   |
  |       £       |  & pound;   |    &# 163;    | 파운드화 |
  |       ¥       |   & yen;    |    &# 165;    |   엔화   |
  |       €       |   & euro;   |   &# 8364;    |  유로화  |
  |       ©       |   & copy;   |    &# 169;    |  저작권  |
  |       ®       |   & reg;    |    &# 174;    | 등록상표 |
  |       ×       |  & times;   |    &# 215;    |   곱셈   |
  |       ÷       |  & divide;  |    &# 247;    |  나눗셈  |



### 7) 문자셋

#### 문자셋

- 웹 브라우저가 HTML 문서를 정확하게 나타내기 위해서는 해당 문서가 어떤 문자셋으로 저장되었는지 알아야 한다.
- HTML 문서가 저장될 때 사용된 문자셋에 대한 정보를 <head>태그 내의 <meta>태그에 명시한다.

#### 문자셋의 종류

1. ASCII : 가장 처음 만들어진 문자셋으로, 인터넷에서 사용할 수 있는 127개의 영문자와 숫자로 이루어져 있음

2. ANSI : 윈도우즈에서 만든 문자셋으로, 총 256개의 문자 코드를 지원

3. ISO-8859-1 : 256개의 문자 코드를 지원하는 HTML4의 기본 문자셋

4. UTF-8 : 세상에 있는 거의 모든 문자를 표현할 수 있는 유니코드 문자를 지원하는 HTML5의 기본 문자셋



## 3. HTML 기본 요소

### 1) 스타일

#### HTML 스타일(Style)

- HTML 요소(element)의 style 속성(attribute)을 이용하면 CSS 스타일을 HTML 요소에 직접 설정 가능
- 하지만 이런 방법은 오직 단 하나의 HTML 요소에만 스타일 적용
- style 속성값에 사용되는 CSS 속성(property)과 속성값들은 세미콜론(;)을 이용하여 구분
- CSS 속성을 하나만 사용할 때나, 여러 개의 CSS 속성 중 맨 마지막 CSS 속성은 세미콜론(;) 생략 가능

- 문법

  ```
  <태그이름 style="속성이름:속성값">
  ```

#### 배경색 변경

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Styles</title>
</head>

<body style="background-color:#33CCFF">

	<h1 style="background-color:white">
		style 속성을 이용한 배경색 변경
	</h1>

</body>

</html>
```

<img alt="result20" src="https://user-images.githubusercontent.com/58800295/87108340-0bb09f80-c29d-11ea-80f5-70db7851903c.PNG">

#### 글자색 변경

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Styles</title>
</head>

<body>

	<h1 style="color:magenta">
		style 속성을 이용한 글자색 변경
	</h1>

</body>

</html>
```

<img alt="result21" src="https://user-images.githubusercontent.com/58800295/87108356-1703cb00-c29d-11ea-833b-f7a9614df88a.PNG">

#### 글자 크기 변경

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Styles</title>
</head>

<body>
	<h1>style 속성을 이용한 글자 크기 변경</h1>
	<h1 style="font-size:250%">
		style 속성을 이용한 글자 크기 변경
	</h1>

</body>

</html>
```

<img alt="result22" src="https://user-images.githubusercontent.com/58800295/87108378-22ef8d00-c29d-11ea-8888-924f453d88c1.PNG">

#### 문단 정렬 변경

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Styles</title>
</head>

<body>
	<h1>style 속성을 이용한 문단 정렬 변경</h1>
	<h1 style="text-align:center">
		style 속성을 이용한 문단 정렬 변경
	</h1>

</body>

</html>
```

<img alt="result23" src="https://user-images.githubusercontent.com/58800295/87108538-88dc1480-c29d-11ea-8d55-ff581ee1c982.PNG">

#### 여러 스타일의 설정

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Styles</title>
</head>

<body style="background-color:#33CCFF">
	<h1>style 속성을 이용하여 한 번에 스타일링 하기!</h1>
	<h1 style="background-color:white; color:pink; font-size:150%; text-align:center">
		style 속성을 이용하여 한 번에 스타일링 하기!
	</h1>

</body>

</html>
```

<img alt="result24" src="https://user-images.githubusercontent.com/58800295/87108542-8aa5d800-c29d-11ea-9abb-be685bdbeaf4.PNG">



### 2) 색상

#### 색 표현 방법

1. 색상 이름으로 표현

2. RGB 색상값으로 표현

3. 16진수 색상값으로 표현

#### 색상 이름으로 표현

<img alt="color" src="https://user-images.githubusercontent.com/58800295/87108602-a7daa680-c29d-11ea-8e1d-59e52ce69ee8.PNG">

```html
<!DOCTYPE html>
<html lang="ko">

<head>
	<meta charset="UTF-8">
	<title>HTML Color</title>
</head>

<body>

	<h1 style="color:blue">색상 이름으로 표현된 파란색</h1>
	<h1 style="color:green">색상 이름으로 표현된 녹색</h1>
	<h1 style="color:silver">색상 이름으로 표현된 은색</h1>
	<h1 style="color:teal">색상 이름으로 표현된 청록색</h1>
	<h1 style="color:red">색상 이름으로 표현된 빨간색</h1>

</body>

</html>
```

<img alt="result25" src="https://user-images.githubusercontent.com/58800295/87108546-8c6f9b80-c29d-11ea-90c2-d4c0c2f96377.PNG">

- 현재는 주요 브라우저가 140개의 색상 이름을 모두 지원

#### RGB 색상값으로 표현

- 모니터와 스크린은 빨간색(Red), 녹색(Green), 파란색(Blue)을 혼합해 색을 표현

- HTML에서도 이처럼 세 가지 색을 가지고 색을 표현하는 RGB 색상을 사용

- RGB 색상의 기본색은 각각 0부터 255까지의 범위를 가지고 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Color</title>
  </head>
  
  <body>
  
  	<h1 style="color:rgb(0,0,255)">RGB 색상값으로 표현된 파란색</h1>
  	<h1 style="color:rgb(0,128,0)">RGB 색상값으로 표현된 녹색</h1>
  	<h1 style="color:rgb(192,192,192)">RGB 색상값으로 표현된 은색</h1>
  	<h1 style="color:rgb(0,128,128)">RGB 색상값으로 표현된 청록색</h1>
  	<h1 style="color:rgb(255,0,0)">RGB 색상값으로 표현된 빨간색</h1>
  
  </body>
  
  </html>
  ```

  <img alt="result26" src="https://user-images.githubusercontent.com/58800295/87108551-8da0c880-c29d-11ea-8a95-8d8b11cac48c.PNG">

#### 16진수 색상값으로 표현

- 16진수 색상값은 RGB 색상값을 각각 16진수로 변환한 것

- 따라서 각각의 기본색은 각각 00부터 FF까지의 범위를 가진다.

- 예를 들면, 빨간색을 나타내는 RGB 색상값인 rgb(255,0,0)은 16진수 색상값으로는 #FF0000이 되는 것

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Color</title>
  </head>
  
  <body>
  
  	<h1 style="color:#0000FF">16진수 색상값으로 표현된 파란색</h1>
  	<h1 style="color:#008000">16진수 색상값으로 표현된 녹색</h1>
  	<h1 style="color:#C0C0C0">16진수 색상값으로 표현된 은색</h1>
  	<h1 style="color:#008080">16진수 색상값으로 표현된 청록색</h1>
  	<h1 style="color:#FF0000">16진수 색상값으로 표현된 빨간색</h1>
  
  </body>
  
  </html>
  ```

  <img alt="result27" src="https://user-images.githubusercontent.com/58800295/87108553-8ed1f580-c29d-11ea-907a-9704636c540b.PNG">



### 3) 배경

- 기본 배경(background)은 흰색이다.
- HTML에서는 이런 배경을 다음과 같이 변경할 수 있다.
  1. 배경을 다른 색으로 변경
  2. 배경을 다른 이미지로 변경

#### 배경을 다른 색으로 변경

- HTML5 이전에는 **bgcolor** 속성을 사용해 HTML 요소의 배경색을 다른 색으로 변경

- **현재는** bgcolor 속성을 더 이상 지원하지 않으며, **CSS를 이용해 배경색을 변경**하도록 한다.

- CSS 스타일을 이용하여 배경색을 다른 색으로 변경하는 예제

  ```css
  <style>
  
      body { background-color: lightblue; }
  
      h1 { background-color: rgb(255,128,0); }
  
      p { background-color: #FFFFCC; }
  
  </style>
  ```

#### 배경을 다른 이미지로 변경

- 문법

  ```
  <태그이름 background="이미지주소">
  ```

- 예제

  ```
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Backgrounds</title>
  </head>
  
  <body background="/examples/images/img_background_good.png">
  
  	<h1>배경으로 이미지 삽입하기</h1>
  
  </body>
  
  </html>
  ```

  <img alt="result28" src="https://user-images.githubusercontent.com/58800295/87108748-f6884080-c29d-11ea-86c2-123201360a75.PNG">

- 배경을 이미지로 사용하면 웹 페이지의 로딩시간이 증가
- 따라서 보통은 작은 사이즈의 이미지를 패턴으로 만들어 배경이미지로 반복설정



### 4) 링크

- 오늘날 웹페이지에는 다른 페이지나 다른 사이트로 연결되는 수많은 하이퍼 링크가 존재

- 이런 **하이퍼 링크**를 간단히 **링크(link)**라고도 부르며, HTML에서는 **<a>태그**로 표현

- 문법

  ```html
  <a href="링크 주소">HTML 링크</a>
  ```

  - <a> 태그의 href 속성은 링크를 클릭하면 연결할 페이지나 사이트의 url 주소 명시

  - <a> 태그는 텍스트나 단락, 이미지 등 다양한 HTML 요소에서 활용

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    
    <head>
    	<meta charset="UTF-8">
    	<title>HTML Links</title>
    </head>
    
    <body>
    
    	<h1>a태그로 링크 걸기</h1>
    	<a href="/html/intro">
    		<h2>이 링크를 클릭해 보세요!</h2>
    	</a>
    
    </body>
    
    </html>
    ```

    <img alt="result29" src="https://user-images.githubusercontent.com/58800295/87108751-f720d700-c29d-11ea-9440-3cfc892358c0.PNG">

#### 타겟 속성

- <a> 태그의 **target** 속성은 링크로 연결된 문서를 어디에서 열 지를 명시

  |   target 속성값    |                             설명                             |
  | :----------------: | :----------------------------------------------------------: |
  |       _blank       |         링크로 연결된 문서를 새 창이나 새 탭에서 염.         |
  |       _self        |  링크로 연결된 문서를 현재 프레임(frame)에서 염. (기본설정)  |
  |      _parent       |       링크로 연결된 문서를 부모 프레임(frame)에서 염.        |
  |        _top        | 링크로 연결된 문서를 현재 창의 가장 상위 프레임(frame)에서 염. |
  | 프레임(frame) 이름 |      링크로 연결된 문서를 지정된 프레임(frame)에서 염.       |

- 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Links</title>
  </head>
  
  <body>
  
  	<h1>a태그의 target 속성값</h1>
  	<h2><a href="/html/intro" target="_blank">blank</a></h2>
  	<h2><a href="/html/intro" target="_self">self</a></h2>
  	<h2><a href="/html/intro" target="_parent">parent</a></h2>
  	<h2><a href="/html/intro" target="_top">top</a></h2>
  	<h2><a href="/html/intro" target="myframe">myframe</a></h2>
  	<iframe name="myframe" style="width:50%; height: 330px"></iframe>
  
  </body>
  
  </html>
  ```

  <img alt="result30" src="https://user-images.githubusercontent.com/58800295/87108754-f720d700-c29d-11ea-84da-66dae893e055.PNG">

#### 링크의 상태(status)

- HTML 링크의 상태는 다음과같이 네 가지로 구분할 수  있다.

  | 링크의 상태 |                     설명                      |
  | :---------: | :-------------------------------------------: |
  |    link     | 아직 한 번도 방문한 적이 없는 상태 (기본설정) |
  |   visited   |       한 번이라도 방문한 적이 있는 상태       |
  |    hover    |       링크 위에 마우스를 올려놓은 상태        |
  |   active    |       링크를 마우스로 누르고 있는 상태        |

- 웹 브라우저에서 링크가 연결되어 있는 텍스트의 색상은 다음과 같다.

  - default :  밑줄과 텍스트 색상이 파란색
  - visited : 밑줄과 텍스트 색상이 보라색
  - active : 밑줄과 텍스트 색상이 빨간색 (클릭 시)

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Links</title>
  
  	<style>
  		a:link    { color: teal; }
  		a:visited { color: maroon; text-decoration: none }
  		a:hover   { color: yellow; text-decoration: none }
  		a:active  { color: red; text-decoration: none }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>링크의 상태</h1>
  	<h2><a href="/html/intro">링크의 상태에 따라 스타일을 다르게 설정합니다!</a></h2>
  
  </body>
  
  </html>
  ```

#### 페이지 책갈피

- <a> 태그의 **name 속성**을 이용하면 간단한 책갈피를 만들 수 있다.

- 가고 싶은 위치에 <a> 태그를 만들고 name 속성을 작성한다.

- 그 다음 작성한 name 속성값을 이용해 다른 <a> 태그에서 링크를 걸면 된다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Links</title>
  </head>
  
  <body>
  
  	<h1>페이지 책갈피</h1>
  	<a href="#bookmark"><p>제목 7로 간다!</p></a>
  
  	<h2>제목 1</h2>
  	<p>첫 번째 단락</p>
  
  	<h2>제목 2</h2>
  	<p>두 번째 단락</p>
  
  	<h2>제목 3</h2>
  	<p>세 번째 단락</p>
  
  	<h2>제목 4</h2>
  	<p>네 번째 단락</p>
  
  	<h2>제목 5</h2>
  	<p>다섯 번째 단락</p>
  
  	<h2>제목 6</h2>
  	<p>여섯 번째 단락</p>
  
  	<h2 name="bookmark">제목 7</h2>
  	<p>일곱 번째 단락</p>
  
  	<h2>제목 8</h2>
  	<p>여덟 번째 단락</p>
  
  	<h2>제목 9</h2>
  	<p>아홉 번째 단락</p>
  
  
  </body>
  
  </html>
  ```

  

### 5) 이미지

#### HTML 이미지

- 웹 페이지에서 주로 사용되는 이미지의 종류

  |                         JPEG 이미지                          |                          GIF 이미지                          |                          PNG 이미지                          |
  | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | <img src="http://tcpschool.com/lectures/jpg_ex_img.jpg" alt="jpg" style="width:50%;" /> | <img src="http://tcpschool.com/lectures/gif_ex_img.gif" alt="gif" style="zoom:150%;" /> | <img src="http://tcpschool.com/lectures/png_ex_img.png" alt="png" style="width:50%;" /> |

#### 이미지 삽입

- 이미지를 삽입할 때는 <img> 태그를 이용

- <img> 태그는 종료 태그가 없는 **빈 태그(empty tag)**이고, 다음과 같은 문법으로 사용

- 문법

  ```
  <img src="이미지주소" alt="대체문자열">
  ```

  - **src 속성** : 이미지가 저장된 주소의 **url 주소**를 명시

  - **alt 속성** : 이미지가 로딩될 수  없는 상황에서 **이미지 대신 나타날 문자열** 설정

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    
    <head>
    	<meta charset="UTF-8">
    	<title>HTML Images</title>
    </head>
    
    <body>
    
    	<h1>img태그의 alt 속성</h1>
    	<img src="/img_html5_logo.png" alt="이미지 없음">
    
    </body>
    
    </html>
    ```

    ![result31](C:\git_repo\HTML5\90\media\result31.PNG)

#### 이미지의 크기(width, height) 설정

- **width** 속성과 **height** 속성을 이용하면, 이미지의 너비와 높이를 각각 **픽셀(pixel) 단위**로 설정

- 나중에 배우게 될 CSS를 이용한 내부 스타일 시트나 외부 스타일 시트와 상관없이 이미지의 원래 크기를 유지하려면 style 속성을 사용하는 것이 좋다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Images</title>
  	<style>
  		img {
  			width:100%;
  			border: solid 1px black;
  		}
  	</style>
  </head>
  
  <body>
  
  	<h1>이미지의 크기 설정</h1>
  	<img src="/examples/images/img_flag.png" alt="html size" width="320" height="214">
  	<img src="/examples/images/img_flag.png" alt="style size" style="width:320px; height:214px">
  
  </body>
  
  </html>
  ```

  ![결과 32](C:\git_repo\HTML5\90\media\result32.PNG)

#### 이미지의 테두리(border) 설정

- 예제

  ```html
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Images</title>
  </head>
  
  <body>
  
  	<h1>이미지의 테두리 설정</h1>
  	<img src="/examples/images/img_flag.png" alt="이미지 테두리" style="width:320px; height:214px; border: 3px solid black">
  
  </body>
  
  </html>
  ```

  ![결과 33](C:\git_repo\HTML5\90\media\result33.PNG)

#### 이미지에 링크(link)  설정

- 예제

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>TCPSchool HTML Images</title>
  </head>
  
  <body>
  
  	<h1>이미지에 링크 설정</h1>
  
  	<a href="/html/intro">
  		<img src="/examples/images/img_flag.png" alt="flag" 
               style="width:320px; height:214px; border: 1px solid black">
  	</a>
  	<p>이미지를 클릭해 보세요!</p>
  
  </body>
  
  </html>
  ```

#### 이미지 맵 만들기

- HTML에서는 **<map>태그를 이용**하여 이미지 맵(image map)을 제작

- 이미지 맵(image map)이란 **이미지의 일부를 클릭할 수 있도록 만들어서 버튼처럼 사용**하는 기능을 의미

- <img>태그의 **usemap** 속성을 <map>태그의 **name** 속성과 연결하면 **이미지와 맵 사이의 관계**가 설정

- HTML <map>태그는 **하나 이상의 <area>태그**를 가지며, 이 **<area>태그가 바로 버튼**과 같은 역할

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Images</title>
  </head>
  
  <body>
  
  	<h1>이미지 맵 만들기</h1>
  	<img src="/examples/images/img_imagemap.jpg" alt="진실혹은거짓"
           usemap="#vending" style="width:320px; height:240px" />
  	<map name="vending"> 
  		<area shape="rect" coords="90,60,180,130" alt="거짓"
                href="https://ko.wikipedia.org/wiki/%EA%B1%B0%EC%A7%93%EB%A7%90">
  		<area shape="rect" coords="210,200,70,130" alt="진실"
                href="https://ko.wikipedia.org/wiki/%EC%A7%84%EC%8B%A4">
  	</map>
  	<p>표지판을 눌러보세요!</p>
  
  </body>

  </html>
  ```
  
  

### 6) 리스트

#### HTML 리스트(list)

- 여러 요소들을 일렬로 나열한  목록이나 명단을 의미
- HTML에서 제공하는 리스트
  - 순서가 없는 리스트(unordered list)
  - 순서가 있는 리스트(ordered list)
  - 정의 리스트(definition list)

#### 순서가 없는 리스트(Unordered list)

- 순서가 없는 리스트는 **<ul>태그**로 시작

- 여기에 포함되는 각각의 리스트 요소는 **<li>태그**로 시작

- 각각의 리스트 요소 앞에는 기본 마커(marker)로 **검정색의 작은 원(bullet)**이 위치

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Lists</title>
  </head>
  
  <body>
  
  	<h1>순서가 없는 리스트</h1>
  	<ul>
  		<li>사과</li>
  		<li>멜론</li>
  		<li>바나나</li>
  	</ul>
  
  </body>
  
  </html>
  ```

  ![결과34](C:\git_repo\HTML5\90\media\result34.PNG)

- CSS의 **list-style-type** 속성을 사용하면 리스트 요소 앞에 위치하는 마커(marker)를 다른 모양으로 변경 가능

  - disc : 검정색 작은 원 모양(default)
  - circle : 흰색 작은 원 모양
  - square : 사각형 모양

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Lists</title>
  </head>
  
  <body>
  
  	<h1>순서가 없는 리스트</h1>
  	<p>검정색 작은 원 모양 (기본설정)</p>
  	<ul>
  		<li>사과</li>
  		<li>멜론</li>
  		<li>바나나</li>
  	</ul>
  
  	<p>흰색 작은 원 모양</p>
  	<ul style="list-style-type: circle">
  		<li>수박</li>
  		<li>참외</li>
  		<li>옥수수</li>
  	</ul>
  
  	<p>검정색 사각형 모양</p>
  	<ul style="list-style-type: square">
  		<li>감자</li>
  		<li>상추</li>
  		<li>고구마</li>
  	</ul>
  
  </body>
  
  </html>
  ```

  ![결과 35](C:\git_repo\HTML5\90\media\result35.PNG)

#### 순서가 있는 리스트(Ordered list)

- 순서가 있는 리스트는 **<ol> 태그**로 시작

- 각각의 리스트 요소는 **<li> 태그**로 시작

- 각각의 리스트 요소 앞에는 **기본 마커로 아라비아 숫자**가 위치

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Lists</title>
  </head>
  
  <body>
  
  	<h1>순서가 있는 리스트</h1>
  	<ol>
  		<li>사과</li>
  		<li>멜론</li>
  		<li>바나나</li>
  	</ol>
  
  </body>
  
  </html>
  ```

  ![결과 36](C:\git_repo\HTML5\90\media\result36.PNG)

- CSS의 **list-style-type** 속성을 사용하면 리스트 요소 앞에 위치하는 마커(marker)를 다른 모양으로 변경 가능

  - demical : 숫자(default)
  - upper-alpha : 영문 대문자
  - lower-alpha : 영문 소문자
  - upper-roman : 로마 숫자 대문자
  - lower-romans : 로마 숫자 소문자

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Lists</title>
  </head>
  
  <body>
  
  	<h1>순서가 있는 리스트</h1>
  	<p>숫자 (기본설정)</p>
  		<ol>
  			<li>사과</li>
  			<li>멜론</li>
  			<li>바나나</li>
  		</ol>
  
  	<p>영어 대문자</p>
  		<ol style="list-style-type: upper-alpha">
  			<li>수박</li>
  			<li>참외</li>
  			<li>옥수수</li>
  		</ol>
  
  	<p>영어 소문자</p>
  		<ol style="list-style-type: lower-alpha">
  			<li>감자</li>
  			<li>상추</li>
  			<li>고구마</li>
  		</ol>
  
  	<p>로마자 대문자</p>
  		<ol style="list-style-type: upper-roman">
  			<li>오이</li>
  			<li>배추</li>
  			<li>시금치</li>
  		</ol>
  		
  	<p>로마자 소문자</p>
  		<ol style="list-style-type: lower-roman">
  			<li>고추</li>
  			<li>호박</li>
  			<li>양파</li>
  		</ol>
  	</p>
  
  </body>
  
  </html>
  ```

  ![결과 37](C:\git_repo\HTML5\90\media\result37.PNG)

#### 정의 리스트(Definition list)

- 정의 리스트는 **용어와 그에 대한 정의를 모아놓은** 리스트

- 리스트는 **<dl>** 태그로 시작

- **<dt> 태그**에는 **용어의 이름**

- **<dd> 태그**에는 **해당 용어에 대한 정의**

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Lists</title>
  </head>
  
  <body>
  
  	<h1>정의 리스트</h1>
  	<dl>
  		<dt>호박</dt>
  		<dd>- 박과의 한해살이 덩굴성 채소</dd>
  		<dt>상추</dt>
  		<dd>- 국화과의 한해살이 또는 두해살이풀</dd>
  	</dl>
  
  </body>
  
  </html>
  ```

  ![결과 38](C:\git_repo\HTML5\90\media\result38.PNG)



### 7) 테이블

#### HTML 테이블(table)

- 테이블(table)이란 여러 종류의 데이터(data)를 보기 좋게 정리해 보여주는 **표**를 의미

- 테이블(table) 태그

  - **<tr> 태그** : 테이블의 **열** 구분
  - **<th> 태그** : 각 **열의 제목**, 모든 내용은 자동으로 굵은 글씨에 가운데 정렬이 됨
  - **<td> 태그** : 테이블의 열을 **각각의 셀**(cell)로 나누어줌

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  </head>
  
  <body>
  
  	<h1>테이블 만들기</h1>
  	<table style="width:100%">
  		<tr style="background-color:lightgrey">
  			<th>참치</th>
  			<th>고래</th>		
  			<th>날치</th>
  		</tr>
  		<tr>
  			<td>상어</td>
  			<td>문어</td>		
  			<td>꽁치</td>
  		</tr>
  		<tr>
  			<td>오징어</td>
  			<td>고등어</td>		
  			<td>돌고래</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 39](C:\git_repo\HTML5\90\media\result39.PNG)

- CSS의 **border** 속성을 이용해 테이블에 테두리를 표시

  - border 속성 값을 따로 명시하지 않으면 해당 테이블은 **언제나 빈 테두리**를 가지게 됨

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  	<style>
  		table, th, td { border: 1px solid black }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>다양한 테이블 테두리</h1>
  	<table style="width:100%">
  		<tr style="background-color:lightgrey">
  			<th>참치</th>
  			<th>고래</th>		
  			<th>날치</th>
  		</tr>
  		<tr>
  			<td>상어</td>
  			<td>문어</td>		
  			<td>꽁치</td>
  		</tr>
  		<tr>
  			<td>오징어</td>
  			<td>고등어</td>		
  			<td>돌고래</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 40](C:\git_repo\HTML5\90\media\result40.PNG)

  - 위의 코드에서 테이블의 border가 2줄씩 나타나는 이유는 <table> 태그와 <th> 태그, <td> 태그가 **모두 자신만의 테두리**를 가지고 있기 때문
  - 2줄에서 1줄로 설정하기 위해서는 **border-collapse** 속성을 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  	<style>
  		table, th, td {	border: 1px solid black; border-collapse: collapse }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>일반적인 테이블 만들기</h1>
  	<table style="width:100%">
  		<tr style="background-color:lightgrey">
  			<th>참치</th>
  			<th>고래</th>		
  			<th>날치</th>
  		</tr>
  		<tr>
  			<td>상어</td>
  			<td>문어</td>		
  			<td>꽁치</td>
  		</tr>
  		<tr>
  			<td>오징어</td>
  			<td>고등어</td>		
  			<td>돌고래</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 41](C:\git_repo\HTML5\90\media\result41.png)

#### 테이블의 열 합치기

- **colspan** 속성을 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  	<style>
  		table, th, td {	border: 1px solid black; border-collapse: collapse }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>테이블의 열 합치기</h1>
  	<table style="width:100%">
  		<tr>
  			<td>참치</td>
  			<td colspan="2">고래</td>		
  		</tr>
  		<tr>
  			<td>상어</td>
  			<td>문어</td>		
  			<td>꽁치</td>
  		</tr>
  		<tr>
  			<td>오징어</td>
  			<td>고등어</td>		
  			<td>돌고래</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 42](C:\git_repo\HTML5\90\media\result42.PNG)

#### 테이블의 행 합치기

- **rowspan** 속성 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  	<style>
  		table, th, td {	border: 1px solid black; border-collapse: collapse }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>테이블의 행 합치기</h1>
  	<table style="width:100%">
  		<tr>
  			<td>참치</td>
  			<td>고래</td>
  			<td>날치</td>		
  		</tr>
  		<tr>
  			<td rowspan="2">상어</td>
  			<td>문어</td>		
  			<td>꽁치</td>
  		</tr>
  		<tr>
  			<td>고등어</td>		
  			<td>돌고래</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 43](C:\git_repo\HTML5\90\media\result43.PNG)

#### 테이블의 열과 행 합치기

- colspan과 rowspan 속성을 사용하면 복잡한 테이블도 표현 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Tables</title>
  	<style>
  		table, th, td {	border: 1px solid black; border-collapse: collapse }
  	</style>
  
  </head>
  
  <body>
  
  	<h1>테이블의 열과 행 합치기</h1>
  	<table style="width:100%">
  		<tr>
  			<td>1</td>
            	<td>2</td>
            	<td>3</td>
            	<td>4</td>
            	<td>5</td>
            	<td>6</td>
            
  		</tr>
  		<tr>
  			<td colspan="6">2</td>
  		</tr>
  		<tr>
  			<td rowspan="3">3</td>
  			<td rowspan="3">4</td>
  			<td colspan="2">5</td>
  			<td>6</td>
  			<td>7</td>
  		</tr>
  		<tr>
  			<td colspan="3">8</td>
  			<td>9</td>
  		</tr>
  		<tr>
  			<td colspan="4">10</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 44](C:\git_repo\HTML5\90\media\result44.PNG)



## 4. HTML 공간 분할

### 1) 블록과 인라인

#### HTML 요소의 타입

- HTML의 모든 요소는 해당 요소가 웹 브라우저에 어떻게 보이는가를 결정짓는 **display** 속성을 가진다.
- display 속성 값
  - 블록(block)
  - 인라인(inline)

#### 블록(block) 타입의 요소

- display 속성 값이 블록(block)인 요소는 언제나 새로운 라인(line)에서 시작

- 해당 라인의 모든 너비를  차지

- 대표적 요소로는 <p>, <div>, <h>, <ul>, <ol>, <form> 요소가 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Block Inline</title>
  </head>
  
  <body>
  
  	<h1>display 속성값 : 블록</h1>
  	<p style="border: 3px solid red">
  		p요소는 대표적인 display 블록(block) 속성 값을 갖고 있다.
  	</p>
  
  </body>
  
  </html>
  ```

  ![결과 45](C:\git_repo\HTML5\90\media\result45.PNG)

##### &lt;div&gt; 요소

- &lt;div&gt; 요소는 다른 HTML 요소를 하나로 묶는 데에 자주사용되는 대표적인 블록(block) 요소

- &lt;div&gt; 요소는 주로 여러 요소들의 스타일을 한 번에 적용하기 위해 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Block Inline</title>
  </head>
  
  <body>
  
  	<div style="background-color:lightgrey; color:green; text-align:center">
  		<h1>div요소를 이용한 스타일 적용</h1>
  		<p>이렇게 div요소로 여러 요소들을 묶은 다음에 style 속성과 클래스 등을 이용하여
  		한 번에 스타일을 적용할 수 있으며, <br> 회색 바탕으로 적용된 부분이 전부 div이다.</p>
  	</div>	
  
  </body>
  
  </html>
  ```

  ![결과 46](C:\git_repo\HTML5\90\media\result46.PNG)

#### 인라인(inline) 타입의 요소

- display 속성값이 인라인(inline)인 요소는 **새로운 라인(line)에서 시작하지 않는다.**

- 또한, 요소의 너비도 해당 라인 전체가 아닌 **해당 HTML 요소의 내용(content) 만큼만 차지**

- 대표적 요소로는 &lt;span&gt;, &lt;a&gt;, &lt;img&gt; 가 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Block Inline</title>
  </head>
  
  <body>
  
  	<h1>display 속성값 : 인라인</h1>
  	<p><span style="background-color:grey; color:orange">span요소</span>는 display 속성값이 인라인인 요소입니다.</p>
  
  </body>
  
  </html>
  ```

  ![결과 47](C:\git_repo\HTML5\90\media\result47.PNG)

##### &lt;span&gt; 요소

- &lt;span&gt; 요소는 **텍스트(text) 특정 부분을 묶는 데에 자주 사용**되는 인라인(inline) 요소

- &lt;span&gt; 요소는 주로 텍스트의 **특정 부분에 따로 스타일을 적용**하기 위해 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Block Inline</title>
  </head>
  
  <body>
  
  	<h1>span요소를 이용한 스타일 적용</h1>
  	<p>이렇게 
  	<span style="border: 3px solid red">span요소로 텍스트의 일부분</span>
  	만을 따로 묶은 후에 스타일을 적용할 수 있습니다.</p>
  
  </body>
  
  </html>
  ```

  ![결과 48](C:\git_repo\HTML5\90\media\result48.PNG)



### 2) iframe 요소

#### iframe 요소

- inline frame의 약자

- iframe 요소를 이용하면 해당 웹 페이지 안에 어떠한 제한 없이 또 다른 하나의 웹페이지를 삽입

- 문법

  ```html
  <iframe src="삽입할 페이지 주소"></iframe>
  ```

- frame 요소와는 달리 종료 태그가 존재

- 명시된 크기로 삽입되는 창의 크기가 고정됨

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Iframes</title>
  </head>
  
  <body>
  
  	<h1>iframe태그를 이용한 웹 페이지 삽입</h1>
  	<iframe src="/css/intro" style="width:100%; height:300px"></iframe>
  
  </body>
  
  </html>
  ```

  ![결과 49](C:\git_repo\HTML5\90\media\result49.PNG)

#### iframe 요소의 테두리 변경

- 기본적으로 검은색 테두리(border)를 가짐

- 테두리의 스타일은 style 속성에서 border 속성을 이용하면 변경 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Iframes</title>
  </head>
  
  <body>
  
  	<h1>iframe의 테두리 변경</h1>
  	<iframe src="/css/intro" style="width:100%; height:300px; border: 5px dashed pink"></iframe>
  
  </body>
  
  </html>
  ```

  ![결과 50](C:\git_repo\HTML5\90\media\result50.PNG)

- 테두리를 표현하고 싶지 않은 경우에는 style 속성에서 border 값을 none으로 변경하면 된다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Iframes</title>
  </head>
  
  <body>
  
  	<h1>iframe의 테두리 삭제</h1>
  	<iframe src="/css/intro" style="width:100%; height:300px; border:none"></iframe>
  
  </body>
  
  </html>
  ```

  ![결과 51](C:\git_repo\HTML5\90\media\result51.PNG)

#### iframe 요소의 페이지 변경하기

- &lt;a&gt; 태그를 이용하면 iframe 요소의 최초 페이지를 중간에 변경 가능

- &lt;a&gt; 태그의 target 속성과 iframe 요소의 name 속성을 연결하면, &lt;a&gt; 태그를 통해 iframe 요소의 페이지를 변경할 수 있게 됨

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Iframes</title>
  </head>
  
  <body>
  
  	<h1>iframe 요소의 페이지 변경하기</h1>
  	<iframe src="/css/intro" name="frame_target" style="width:100%; height:400px"></iframe>
  	<p><a href="/php/intro" target="frame_target">PHP 수업 확인하러 가기 =></a></p>
  	<p>위의 링크를 클릭하면 iframe 요소의 페이지가 다른 페이지로 변경돼요!</p>
  
  </body>
  
  </html>
  ```

  ![결과 52](C:\git_repo\HTML5\90\media\result52.gif)

#### **프레임셋(frameset)

- 프레임셋을 이용하면 하나의 브라우저 창에 둘 이상의 페이지를 표시 가능
- 프레임셋은 iframe 요소와는 달리 하나 이상의 페이지를 동시에 가진다.
- noresize 속성을 명시하지 않으면, 사용자가 마음대로 크기를 조절 가능
- 프레임셋에서 각각의 페이지는 frame 요소로 표현
- frame 요소는 iframe 요소와는 달리 종료 태그가 없다.
- noframes 요소는 해당 브라우저가 frame 요소를 지원하지 않을 때 보여지는 문자열을 저장
- **frameset, frame, noframes 요소는 더는 HTML5 표준 권고안에서 지원하지 않는다.
  따라서 하나의 브라우저 창에 여러 페이지를 표현하고 싶을 때는 iframe 요소를 사용하거나 CSS를 이용하여 표현해야 합니다.**

##### 수직 프레임셋

- 하나의 브라우저 창을 세로 방향으로 분리하여 표현

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Frames</title>
  </head>
  
  
  <frameset cols="25%,*,25%">
  <frame name="left" src="/html/intro"/>
  <frame name="center" src="/css/intro"/>
  <frame name="right" src="/php/intro"/>
  <noframes>
  	<body>
  		이 브라우저는 frame태그를 지원하지 않습니다!
  	</body>
  </noframes>
  </frameset>
  
  </html>
  ```

##### 수평 프레임셋

- 하나의 브라우저 창을 가로 방향으로 분리하여 표현

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Frames</title>
  </head>
  
  <frameset rows="20%,60%,20%">
  <frame name="top" src="/html/intro" noresize="noresize" />
  <frame name="center" src="/css/intro" noresize="noresize" />
  <frame name="bottom" src="/php/intro" noresize="noresize" />
  <noframes>
  	<body>
  		이 브라우저는 frame태그를 지원하지 않습니다!
  	</body>
  </noframes>
  </frameset>
  
  </html>
  ```

  - 위의 예제는 frame 요소에 noresize 속성을 명시하였으므로, 사용자가 창의 크기를 조절할 수 없습니다.

### 3) 레이아웃

#### HTML 레이아웃(Layout)

- 레이아웃이란 특정한 공간에 여러 구성요소를 보기 좋게 효과적으로 배치하는 작업

- 웹 페이지의 레이아웃은 웹 사이트의 외관을 결정짓는 매우 중요한 요소

  ![레이아웃](http://tcpschool.com/lectures/img_html_layout.jpg)

- 레이아웃 작성 방법
  1. div 요소를 이용한 레이아웃
  2. HTML5 레이아웃
  3. table 요소를 이용한 레이아웃

#### div 요소를 이용한 레이아웃

- div 요소는 CSS 스타일을 손쉽게 적용할 수 있으므로 레이아웃을 작성하는 데에 자주 사용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Layouts</title>
  	<style>
  		#header {
  			background-color:lightgrey;
  			height:100px;
  		}
  		#nav {
  			background-color:#339999;
  			color:white;
  			width:200px;
  			height:300px;
  			float:left;
  		}
  		#section {
  			width:200px;
  			text-align:left;
  			float:left;
  			padding:10px;
  		}
  		#footer {
  			background-color:#FFCC00;
  			height:100px;
  			clear:both;
  		}
  		#header, #nav, #section, #footer { text-align:center; }
  		#header, #footer { line-height:100px; }
  		#nav, #section { line-height:240px; }
  	</style>
  </head>
  
  <body>
  
  	<h1>div 요소를 이용한 레이아웃</h1>
  	<div id="header">
  		<h2>HEADER 영역</h2>
  	</div>
  	<div id="nav">
  		<h2>NAV 영역</h2>
  	</div>
  	<div id="section">
  		<p>SECTION 영역</p>
  	</div>
  	<div id="footer">
  		<h2>FOOTER 영역</h2>
  	</div>
  
  </body>
  
  </html>
  ```

  ![결과 53](C:\git_repo\HTML5\90\media\result53.PNG)

#### HTML5 레이아웃

- HTML5에서는 웹 페이지의 레이아웃만을 위한 별도의 새로운 요소들을 제공

- 이런 요소들을 의미(semantic) 요소라고 한다.

  ![HTML5 layout](http://tcpschool.com/lectures/img_html_html5_layout.png)

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Layouts</title>
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
  
  	<h1>HTML5 레이아웃</h1>
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

  ![결과 54](C:\git_repo\HTML5\90\media\result54.PNG)

- HTML5에서 제공하는 레이아웃만을 위한 의미(semantic) 요소

  | 의미 요소 |                             설명                             |
  | :-------: | :----------------------------------------------------------: |
  | <header>  | HTML 문서나 섹션(section) 부분에 대한 헤더(header)를 정의함. |
  |   <nav>   |               HTML 문서의 탐색 링크를 정의함.                |
  | <section> |          HTML 문서에서 섹션(section) 부분을 정의함.          |
  | <article> |   HTML 문서에서 독립적인 하나의 글(article) 부분을 정의함.   |
  |  <aside>  |  HTML 문서에서 페이지 부분 이외의 콘텐츠(content)를 정의함.  |
  | <footer>  | HTML 문서나 섹션(section) 부분에 대한 푸터(footer)를 정의함. |

#### table 요소를 이용한 레이아웃

- table 요소를 이용하여 레이아웃을 작성하는 방법은 오래 전에 사용하던 방식

- 현재는 거의 사용하지 않는다.

- table 요소는 레이아웃을 만들기 위해 설계된 요소가 아니어서 테이블로 작성된 레이아웃은 수정하기가 힘듦

- 되도록이면 table로 레이아웃을 만들지 말아야 한다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Layouts</title>
  </head>
  
  <body>
  
  	<h1>table 요소를 이용한 레이아웃</h1>
  	<table width="100%" style="text-align:center; border:none">
  		<tr>
  			<td colspan="2" style="background-color:lightgrey">
  				<h2>HEADER 영역</h2>
  			</td>
  		</tr>
  		<tr>
  			<td style="background-color:#339999; color:white; width:20%">
  				<h2>NAV 영역</h2>
  			</td>
  			<td style="height:200px; text-align:left">
  				<p>SECTION 영역</p>
  			</td>
  		</tr>
  		<tr>
  			<td colspan="2" style="background-color:#FFCC00">
  				<h2>FOOTER 영역</h2>
  			</td>
  		</tr>
  	</table>
  
  </body>
  
  </html>
  ```

  ![결과 55](C:\git_repo\HTML5\90\media\result55.PNG)

## 5. HTML 입력 양식

### 1) Form 요소

#### form 요소

- 웹 페이지에서는 form 요소를 사용해 사용자로부터 입력을 받음

- 또한 사용자가 입력한 데이터를 서버로 보낼 때에도 form 요소 사용

- 문법

  ```html
  <form action="처리할 페이지 주소" method=GET/POST"></form>
  ```

- action 속성

  - 입력받은 데이터를 처리할 서버 상의 스크립트  파일의 주소 명시

- 폼 핸들러

  - action 속성을 통해 전달 받은 데이터를 처리하는 스크립트 파일
  - 입력 받은 데이터를 처리하기 위한 서버 측의 웹 페이지를 의미

- method 속성

  - 입력받은 데이터를 서버에 전달할 방식을 명시

- 사용자가 form 요소를 통해 입력한 데이터는 action 속성에 명시된 위치로 method 속성의 방식을 통해 전달

#### method 속성

- method 속성을 통해 명시할 수 있는 form 요소의 전달 방식은 GET 방식과 POST 방식으로 나뉨

##### GET 방식

- 주소에 데이터(data)를 추가하여 전달하는 방식
- 데이터가 주소 입력창에 그대로 나타남
- 전송할 수  있는 데이터의 크기 또한 제한적
- 검색 엔진의 쿼리(query)와 같이 크기가 작고 중요도가 낮은 정보를 보낼 때 주로 사용

##### POST 방식

- 데이터(data)를 별도로 첨부하여 전달하는 방식
- 데이터가 외부로 드러나지 않음
- 전송할 수 있는 데이터의 크기가 제한적이지 않음
- 보안성 및 활용성이 GET 방식보다 좋음

#### 다양한 타입의 input 요소

- HTML에서는 다양한 타입의 input 요소를 사용하여 사용자로부터 입력을 받을 수 있다.

#### 대표적인 input 요소의 타입

##### 1. 텍스트 입력(text)

- &lt;input&gt;태그의 type 속성값을 "text"로 설정하면, 사용자로부터 한 줄의 텍스트를 입력 받을 수 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>텍스트 입력</h1>
  	<form action="/examples/media/request.php">
  		검색할 내용을 입력하세요 :
  		<input type="text" name="search">
  	</form>
  </body>
  </html>
  ```

  ![결과 56](C:\git_repo\HTML5\90\media\result56.PNG)

##### 2. 비밀번호 입력(password)

- &lt;input&gt; 태그의 type 속성 값을 "password"로 설정하면, 사용자로부터 비밀번호를 입력받을 수 있다.

- 비밀번호를 입력받기 때문에 화면에는 입력받은 문자나 숫자 대신 별표나 작은 원 모양 표시.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>비밀번호 입력</h1>
  	<form>
  		사용자 : <br>
  		<input type="text" name="username"><br>
  		비밀번호 : <br>
  		<input type="password" name="password">
  	</form>
  </body>
  </html>
  ```

  ![결과 57](C:\git_repo\HTML5\90\media\result57.PNG)

##### 3. 라디오 버튼(radio)

- &lt;input&gt; 태그의 type 속성값을 "radio"로 설정 

- 사용자로부터 여러 개의 옵션(option) 중에서 단 하나의 옵션만을 입력 받을 수 있다.

- 이때 서버로 정확한 입력을 전송하기 위해서는 반드시 모든 input 요소의 name 속성이 같아야 한다.

- checked 속성을 이용해 여러 개의 옵션 중 처음에 미리 선택되는 옵션을 지정할 수 있다.

- 정확한 입력 값 전송을 위해서 radio 타입의 모든 input 요소가 반드시 같은 name 속성을 가지고 있어야 한다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>라디오 버튼</h1>
  	<p>다음 중 가장 재밌고 내용이 알찬 강좌를 하나만 골라주세요.</p>
  	<form>
  		<input type="radio" name="lecture" value="html" checked> HTML <br>
  		<input type="radio" name="lecture" value="css"> CSS <br>
  		<input type="radio" name="lecture" value="java"> JAVA <br>
  		<input type="radio" name="lecture" value="cpp"> C++
  	</form>=
  </body>
  </html>
  ```

  ![결과 58](C:\git_repo\HTML5\90\media\result58.PNG)

##### 4. 체크박스(checkbox)

- &lt;input&gt; 태그의 type 속성 값을 "checkbox"로 설정

- 체크 박스는 라디오 버튼과 달리 여러 개의 옵션 중 다수의 옵션을 한꺼번에 입력 받을 수 있다.

- 서버로 정확한 입력을 전송하기 위해서는 반드시 모든 input 요소의 name 속성이 같아야 한다.

- checked 속성을 이용해 여러 개의 옵션 중 미리 선택되는 옵션을 지정 가능

- disabled 속성을 이용해 해당 옵션을 선택할 수 없게 설정 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>체크박스</h1>
  	<p>다음 중 재밌고 내용이 알찬 강좌를 모두 골라주세요.</p>
  	<form>
  		<input type="checkbox" name="lecture" value="html" checked> HTML <br>
  		<input type="checkbox" name="lecture" value="css"> CSS <br>
  		<input type="checkbox" name="lecture" value="java"> JAVA <br>
  		<input type="checkbox" name="lecture" value="cpp" disabled> C++
  	</form>
  </body>
  </html>
  ```

  ![결과 59](C:\git_repo\HTML5\90\media\result59.PNG)

##### 5. 파일 선택(file)

- &lt;input&gt; 태그의 type 속성 값을 "file"로 설정하면 사용자로부터 파일을 전송 받을 수 있다.

- accept 속성을 이용해 입력 받을 수 있는 파일의 확장자 및 종류를 명시할 수 있다.

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>파일 선택 박스</h1>
  	<p>여러분이 가장 행복했던 날의 사진을 선택해 주세요.</p>
  	<form>
  		<input type="file" name="upload_file" accept="image/*">
  		<!--accept="image/*" : "모든 이미지 파일" 의미-->
  	</form>
  </body>
  </html>
  ```

  ![결과 60](C:\git_repo\HTML5\90\media\result60.PNG)

##### 6. 선택 입력(select)

- select 요소는 여러 개의 옵션이 드롭다운 리스트(drop-down list)로 되어 있다.

- 여러 개의 옵션 중 단 하나의 옵션 만을 입력 받을 수 있다.

- option 요소

  - 드롭다운 리스트에서 선택할 수 있는 각각의 옵션 명시

- selected 속성을 이용해 드롭다운 리스트 중에서 처음에 미리 선택되는 옵션 지정 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>선택 입력</h1>
  	<p>다음 중 여러분이 가장 좋아하는 과일을 골라주세요.</p>
  	<form>
  		<select name="fruit">
  			<option value="apple"> 사과
  			<option value="orange" selected> 귤
  			<option value="strawberry"> 딸기
  			<option value="peach"> 복숭아
  		</select>
  	</form>
  </body>
  </html>
  ```

  ![결과 61](C:\git_repo\HTML5\90\media\result61.PNG)

##### 7. 문장 입력(textarea)

- textarea 요소는 사용자로부터 여러 줄의 텍스트를 입력 받을 수 있다.

- rows 속성과 cols 속성을 이용해 textarea 요소의 크기를 자유롭게 지정 가능

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>문장 입력</h1>
  	<p>여러분의 부모님께 하고 싶은 말을 적어보세요.</p>
  	<form>
  		<textarea name="message" rows="10" cols="50">여기에 적으세요.</textarea>
  	</form>
  </body>
  </html>
  ```

  ![결과 62](C:\git_repo\HTML5\90\media\result62.PNG)

##### 8. 버튼 입력(button)

- button 요소는 사용자가 누를 수 있는 버튼을 나타냄

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>버튼 입력</h1>
  	<button type="button" onclick="alert('버튼을 클릭하셨군요!')">버튼을 눌러주세요.</button>
  </body>
  </html>
  ```

  ![결과 63](C:\git_repo\HTML5\90\media\result63.PNG)

##### 9. 전송 버튼(submit)

- &lt;input&gt; 태그의 type 속성값을 "submit"으로 설정

- 사용자로부터 입력받은 데이터(data)를 서버의 폼 핸들러로 제출하는 버튼을 만들 수 있음

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Forms</title>
  </head>
  <body>
  	<h1>전송 버튼</h1>
  	<form action="/examples/media/request.php">
  		어릴 때 자신의 별명을 적어주세요 : <br>
  		<input type="text" name="nickname" value="별명"><br><br>
  		<input type="submit" value="전송">
  	</form> 
  	<p>별명을 적으신 후에 전송 버튼을 눌러보세요!</p>
  </body>
  </html>
  ```

  ![결과 64](C:\git_repo\HTML5\90\media\result64.gif)

##### 10. 필드셋(fieldset)

- filedset 요소는 form 요소와 관련된 데이터들을 하나로 묶어주는 역할

- legend 요소

  - fieldset 요소 안에서만 사용할 수 있으며, fieldset 요소의 제목을 나타냄

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    <head>
    	<meta charset="UTF-8">
    	<title>HTML Forms</title>
    </head>
    <body>
    	<h1>필드셋</h1>
    	<form action="/examples/media/request.php">
    		<fieldset>
    			<legend>입력 양식</legend>
    			이름 : <br>
    			<input type="text" name="username"><br>
    			이메일 : <br>
    			<input type="text" name="email"><br><br>
    			<input type="submit" value="전송">
    		</fieldset>
    	</form>
    </body>
    </html>
    ```

    ![결과 65](C:\git_repo\HTML5\90\media\result65.PNG)

#### HTML5에서 추가된 다양 한 타입의 input 요소

1. datalist 요소
2. keygen 요소
3. output 요소

### 2) Input 요소의 속성

#### input 요소의 속성

- input 요소의 여러 속성을 사용하면 사용자가 입력하는 방식을 더욱 다양하게 제어 가능

#### value 속성

- value 속성은 input 요소의 입력 필드(input flied)에 나타나는 **초깃값 설정**

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Input Attributes</title>
  </head>
  <body>
  	<h1>value 속성을 이용한 초기값 설정</h1>
  	<form action="/examples/media/request.php">
  		이름 : <br>
  		<input type="text" name="student_name"><br>
  		학번 : <br>
  		<input type="text" name="student_id"><br>
  		학과 : <br>
  		<input type="text" name="department" value="컴퓨터공학과"><br><br>
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![결과66](C:\git_repo\HTML5\90\media\result66.PNG)

#### readonly 속성

- readonly 속성은 사용자가 입력 필드는 볼 수 있으나, **수정할 수는 없도록** 설정

- disabled 속성과 다른 점은 전송 버튼(submit)을 누르면 초깃값이 서버로 전송

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Input Attributes</title>
  </head>
  <body>
  	<h1>readonly 속성을 이용한 필드값 수정 제한</h1>
  	<form action="/examples/media/request.php">
  		이름 : <br>
  		<input type="text" name="student_name"><br>
  		학번 : <br>
  		<input type="text" name="student_id"><br>
  		학과 : <br>
  		<input type="text" name="department" value="컴퓨터공학과" readonly><br><br>
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![결과 67](C:\git_repo\HTML5\90\media\result67.gif)

#### disabled 속성

- 사용자가 입력 필드를 아예 사용할 수 없도록 설정

- disabled 속성이 설정된 입력 필드는 사용할 수도 없고, 클릭할 수도 없음

- readonly 속성과는 다르게 전송 버튼(submit)을 눌러도 초깃값이 서버로 전송되지 않음

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title> HTML Input Attributes</title>
  </head>
  <body>
  	<h1>disabled 속성을 이용한 필드 사용 제한</h1>
  	<form action="/examples/media/request.php">
  		이름 : <br>
  		<input type="text" name="student_name"><br>
  		학번 : <br>
  		<input type="text" name="student_id"><br>
  		학과 : <br>
  		<input type="text" name="department" value="컴퓨터공학과" disabled><br><br>
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![결과 68](C:\git_repo\HTML5\90\media\result68.gif)

#### maxlength 속성

- maxlength 속성은 입력 필드에 입력할 수 있는 문자의 최대 길이(length)를 설정

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Input Attributes</title>
  </head>
  <body>
  	<h1>maxlength 속성을 이용한 필드의 최대 길이 설정</h1>
  	<form action="/examples/media/request.php">
  		이름 : (이름은 10자까지만 가능해요!)<br>
  		<input type="text" name="student_name" value="홍길동" maxlength="10"><br>
  		학번 : <br>
  		<input type="text" name="student_id"><br><br>
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```

  ![결과 69](C:\git_repo\HTML5\90\media\result69.gif)

#### size 속성

- 입력 필드에 보여지는 input 요소의 크기(size) 설정

- maxlength 속성과는 달리 입력 필드가 한 번에 보여줄 수 있는 문자의 최대 개수만을 의미

- 따라서 입력될 수 있는 문자의 최대 길이는 maxlength 속성값에 따라 달라짐(size 속성과는 무관)

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Input Attributes</title>
  </head>
  <body>
  	<h1>size 속성을 이용한 필드의 크기 설정</h1>
  	<form action="/examples/media/request.php">
  		이름 : <br>
  		<input type="text" name="student_name" value="홍길동" size="30"><br>
  		학번 : <br>
  		<input type="text" name="student_id"><br><br>
  		<input type="submit" value="전송">
  	</form>
  </body>
  </html>
  ```
  
  

#### HTML5에서 추가된 form 요소의 속성

- autocomplete
- novalidate

#### HTML5에서 추가된 input 요소의 속성

- autocomplete
- autofocus
- form
- formaction
- formenctype
- formmethod
- formnovalidate
- formtarget
- height and width
- list
- min and max
- multiple
- pattern (정규식)
- placeholder
- required
- step