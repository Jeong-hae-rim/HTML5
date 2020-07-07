# HTML

## HTML 시작

### 1) HTML 개요

- HTML은 웹 페이지를 만드는 데에 사용하는 언어이다.
- 모든 태그는 이미 정의되어 있고, 각각의 태그와 속성을 사용하기만 하면 된다.



### 2) HTML 기초

- HTML이란?

  - HyperText Markup Language의 약자이다.

    - HyperText : 하이퍼텍스트를 가장 중요한 특징으로 하는
    - Markup : 마크업이라는 형식을 가진
    - Language : 컴퓨터 프로그래밍 언어

  - 웹 페이지는 HTML 문서라고도 불리고, HTML 태그들로 구성된다.

  - 각각의 HTML 태그는 웹 페이지의 디자인이나 기능을 결정하는 데 사용된다.

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

    ![실행화면 1](C:\git_repo\HTML5\90\media\result1.png)

- HTML 태그(tag)

  - 태그 이름을 꺽쇠 괄호(<>)로 감싸서 표현한다.

  - 문법

    ```html
    1. <태그이름> //시작 태그
    2. </태그이름> //종료 태그
    ```

    ```
    <h1>오늘의 명언</h1> //heading1, 줄바꿈을 하자는 약속을 암묵적으로함
    우리 모두는 <strong>자신의 힘</strong>으로 발견한 내용을 가장 쉽게 익힌다. (도널드 커누스)
    ```

    ![결과2](C:\git_repo\HTML5\90\media\result2.PNG)

  - HTML 태그는 보통 시작 태그(start tag, opening tag)와 종료 태그(end tag, closing tag) 한 쌍으로 구성된다.

  - 종료 태그는 시작 태그와 전부 똑같지만 앞에 슬래시(/)가 존재한다.

  - 태그에 따라 시작 태그만 있고 종료 태그는 없는 태그도 존재한다.

    이것을 빈 태그(Empty tag)라고 한다.

    ```html
    <img><br><hr> //이런 태그 같이 종료 태그 없이 시작 태그만을 가지는 태그
    ```

- HTML 작성

  - HTML 문서는 윈도우의 메모장, 리눅스의 vi와 같은 기본 에디터로도 작성할 수 있다.
  - HTML 문서의 작성을 마친 후 확장자를 .html로 저장하면 웹 브라우저에서 바로 확인할 수 있다.



### 3) HTML 기본 구조

다음은 HTML 문서의 기본적인 구조를 보여주는 그림이다.

![구조 1](C:\git_repo\HTML5\90\media\structure.png)

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

  - HTML 문서에 대한 정보(data)로, 웹 브라우저에는 직접적으로 표현되지 않는 정보를 의미

  - ```html
    <title>, <style>, <meta>, <link>, <Script>, <base> 태그 등을 이용하여 표현
    ```

- 타이틀(title)

  - 웹 브라우저의 툴바(toolbar)에 표시된다.
  - 웹 브라우저의 즐겨찾기(favorites)에 추가할 때 즐겨찾기의 제목이 된다.
  - 검색 엔진의 결과 페이지에 제목으로 표시된다.



### 4) HTML 요소 구조

- HTML 요소 구조

  - HTML *요소(element)는 여러 속성을 가질 수 있다.

  - 이러한 *속성(attribute)은 해당 요소에 대한 추가적인 정보를 제공한다.

  - HTML 요소는 시작 태그로 시작해서 종료 태그로 끝난다.

    <img src="C:\git_repo\HTML5\90\media\structure2.PNG" alt="구조 2" />

  - 속성은 HTML 요소 중에서도 언제나 시작 태그 내에서만 정의된다.

  - 속성 명 = 속성 값(value)로 표현된다.

    ```
    <태그이름 속성이름="속성값">
    ```

  - 속성 명에 따라 그 기능이 약속되어 있다.
  - 속성의 순서는 상관 없다. 
  - 태그 자체의 빈약한 기능에 다양한 기능들을 추가할 수 있다.

- 속성 이름은 소문자로

  - HTML5 표준에서는 속성 이름에 대소문자를 구별하지 않는다.
  - 하지만 될 수 있으면 소문자로 작성하는 걸 권장
  - XHTML에서는 속성 이름을 더욱 엄격하게 소문자로만 사용

- 속성 값은 언제나 따옴표로 감싼다

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

    <img src="C:\git_repo\HTML5\90\media\result3.PNG" alt="결과3"/>

  - 위 예제처럼 속성 값에 띄어쓰기가 들어가게 되면 반드시 따옴표를 사용해야 정확한 값을 지정할 수 있다.

  - 속성 값을 감쌀 때는 보통 큰따옴표("")가 사용되며, 작은 따옴표('')도 사용할 수 있다.

## HTML 텍스트 요소

### 1) 제목

- HTML은 제목을 표현할 수 있는 다양한 크기의 h 태그를 제공한다.

- 가장 큰 h1 태그부터 h6 태그까지 다양한 크기로 제목을 표현할 수 있다.

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

  ![결과4](C:\git_repo\HTML5\90\media\result4.PNG)

- h 태그는 제목의 표현이라는 기능 외에도 또 다른 중요한 역할을 한다.
  - 여러 검색 엔진들이 h 태그를 이용해 키워드를 수집하고 내용을 파악
  - HTML 문서에 포함되는 제목은 h 태그로 작성해야만 검색 엔진에 의해 제대로 검색될 확률을 높임
- 종료 태그
  - 대부분 웹 브라우저는 종료 태그를 사용하지 않아도 HTML 문서를 잘 표현해준다.
  - 그러나 종료 태그가 없으면 예상치 못한 오류나 결과가 발생할 수 있다.
  - XHTML이나 XML 같은 문법이 엄격한 언어에서는 종료 태그의 유무를 엄격하게 검사
  - 가급적 종료 태그를 빠뜨리지 않고 코드를 작성해야 한다.



### 2) 단락

#### 단락(paragragh)

- 내용상 끊어서 구분할 수 있는 하나하나의 부분을 의미하며, 문단이라고도 부른다.

- HTML에서는 p 태그를 이용해 이런 단락을 표현한다.

- <p> 태그 위아래로는 약간의 여백(margin)이 자동으로 삽입된다.

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

![결과 5](C:\git_repo\HTML5\90\media\result5.PNG)

#### 띄어쓰기와 줄 나누기

- HTML 코드에서는 띄어쓰기와 줄 나누기를 여러 번 하더라도 웹 브라우저 화면 상에는 전혀 영향을 주지 못한다.

- 웹 브라우저는 여러 번 띄어쓰고 줄 나누기를 해도 오직 하나의 띄어쓰기와 줄로만 인식한다.

- ```
  <br>태그(break line)을 사용하면 새로운 단락을 만들지 않고도 줄을 나눌 수 있다.
  이러한 태그는 종료 태그가 없으므로 빈 태그(empty tag)이다.
  ```

#### 텍스트(text) 서식 미리 정의하기

- HTML 코드에서 작성한 텍스트 서식을 그대로 표현하려면 pre태그를 사용한다.

- pre 태그(preformatted text) 내에 작성된 텍스트의 모든 띄어쓰기와 줄 나누기는 웹 브라우저에 그대로 표현된다.
  pre 태그 내에 작성된 텍스트의 글꼴(font)은 고정폭 글꼴(fixed-width font)로 자동변환된다.

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

  ![결과 6](C:\git_repo\HTML5\90\media\result6.PNG)

#### 수평 가로 구분선

- 단락을 나눌 때나 내용상의 구분을 표현하고자 할 때 사용한다.

- 이렇게 사용되는 수평 가로 구분선을 HTML 코드에서는 <hr> 태그(horizontal rule)로 만든다.

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

  ![결과 7](C:\git_repo\HTML5\90\media\result7.PNG)



### 3) 서식

#### 강조 효과

- 텍스트를 굵게 표현하고 싶을 때 <b>태그(bold text)나 <strong>태그를 사용한다.

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

  ![결과 8](C:\git_repo\HTML5\90\media\result8.PNG)

- <b> 태그는 단순히 화면의 텍스트를 굵게 표현해준다.

  하지만 <strong> 태그는 텍스트를 굵게 표현해줄 뿐 아니라 그 내용이 중요하다는 의미도 함께 담고 있다.

- <i> 태그와 <em> 태그는 이탤릭체를 표현해준다.

  <em> 태그 또한 이탤릭체로 표현해줄 뿐 아니라 그 내용이 중요하다는 의미도 담고 있다.

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

  ![결과 9](C:\git_repo\HTML5\90\media\result9.PNG)

- 검색 엔진은 <strong>태그와 <em>태그를 사용하여 강조된 텍스트를 더 중요하게 인식한다.

#### 하이라이팅 효과

- <mark> 태그는 텍스트에 하이라이팅 효과를 적용시켜준다.

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

  ![결과 10](C:\git_repo\HTML5\90\media\result10.PNG)

#### 삭제 효과

- <del>태그(delete)는 텍스트 중앙에 가로줄을 만들어 텍스트를 지운 것 같은 효과를 내준다.

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

  ![결과 11](C:\git_repo\HTML5\90\media\result11.PNG)

#### 삽입 효과

- <ins>태그(insert)는 텍스트 밑에 가로줄을 만들어 빈칸에 텍스트를 삽입한 효과를 내준다.

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

  ![결과 12](C:\git_repo\HTML5\90\media\result12.PNG)

#### 위첨자와 아래첨자 효과

- 위첨자는 <sup>태그(superscript)를 사용하며, 아래첨자는 <sub>태그(subscirpt)를 사용하여 표현

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

  ![결과 13](C:\git_repo\HTML5\90\media\result13.PNG)



### 4) 인용구

#### 짧은 인용구

- 짧은 인용구는 <q>태그(quotation)를 사용하여 표현하며, 자동으로 앞뒤에 큰따옴표가 붙는다.

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

  ![결과 14](C:\git_repo\HTML5\90\media\result14.PNG)

#### 블록 인용구

- 길이가 긴 인용문의 경우 <blockquote>태그(block quatation)를 사용하여 표현

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

  ![결과 15](C:\git_repo\HTML5\90\media\result15.PNG)

#### 축약형 표현

- 용어의 축약형을 표현하기 위해 <abbr>태그(abbrevitation)를 사용한다.

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

  ![결과 16](C:\git_repo\HTML5\90\media\result16.png)

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

  ![결과 17](C:\git_repo\HTML5\90\media\result17.PNG)



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

- HTML 주석 안에 또 다른 주석을 작성할 수는 없다.

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

  ![결과 18](C:\git_repo\HTML5\90\media\result18.PNG)

- 위의 예제처럼 HTML 주석 안에 또 다른 주석을 삽입할 시 삽입한 주석의 종료 태그를 첫 번째 주석이 자신의 종료 태그로 인식

- 따라서 삽입한 주석의 종료 태그 다음부터 첫 번째 주석의 종료 태그까지 모든 내용이 그대로 웹 페이지에 노출됨



### 6) 엔티티

- HTML에 미리 예약된 몇몇 문자를 HTML 예악어라고 부른다.
- 이런 예약어를 HTML 코드에서 사용하면, 웹 브라우저는 그것을 평소와는 다른 의미로 해석
- 따라서 HTML 예약어를 기존에 사용하던 의미 그대로 사용하기 위해 별도로 만든 문자셋이 엔티티(entity)

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

  ![결과 19](C:\git_repo\HTML5\90\media\result19.PNG)

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

![결과 20](C:\git_repo\HTML5\90\media\result20.PNG)

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

![결과 21](C:\git_repo\HTML5\90\media\result21.PNG)

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

![결과 22](C:\git_repo\HTML5\90\media\result22.PNG)

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

![결과23](C:\git_repo\HTML5\90\media\result23.PNG)

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

![결과 24](C:\git_repo\HTML5\90\media\result24.PNG)



### 2) 색상

#### 색 표현 방법

1. 색상 이름으로 표현

2. RGB 색상값으로 표현

3. 16진수 색상값으로 표현

#### 색상 이름으로 표현

![색상](C:\git_repo\HTML5\90\media\color.PNG)

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

![결과25](C:\git_repo\HTML5\90\media\result25.PNG)

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

  ![결과 26](C:\git_repo\HTML5\90\media\result26.PNG)

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

  ![결과 27](C:\git_repo\HTML5\90\media\result27.PNG)



### 3) 배경

- 기본 배경(background)은 흰색이다.
- HTML에서는 이런 배경을 다음과 같이 변경할 수 있다.
  1. 배경을 다른 색으로 변경
  2. 배경을 다른 이미지로 변경

#### 배경을 다른 색으로 변경

- HTML5 이전에는 bgcolor 속성을 사용해 HTML 요소의 배경색을 다른 색으로 변경

- 현재는 bgcolor 속성을 더 이상 지원하지 않으며, CSS를 이용해 배경색을 변경하도록 한다.

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

  ![결과 28](C:\git_repo\HTML5\90\media\result28.PNG)

- 배경을 이미지로 사용하면 웹 페이지의 로딩시간이 증가
- 따라서 보통은 작은 사이즈의 이미지를 패턴으로 만들어 배경이미지로 반복설정



### 4) 링크

- 오늘날 웹페이지에는 다른 페이지나 다른 사이트로 연결되는 수많은 하이퍼 링크가 존재

- 이런 하이퍼 링크를 간단히 링크(link)라고도 부르며, HTML에서는 <a>태그로 표현

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

    ![결과 29](C:\git_repo\HTML5\90\media\result29.PNG)

#### 타겟 속성

- <a> 태그의 target 속성은 링크로 연결된 문서를 어디에서 열 지를 명시

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

  ![결과 30](C:\git_repo\HTML5\90\media\result30.PNG)

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

- <a> 태그의 name 속성을 이용하면 간단한 책갈피를 만들 수 있다.

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

- <img> 태그는 종료 태그가 없는 빈 태그(empty tag)이고, 다음과 같은 문법으로 사용

- 문법

  ```
  <img src="이미지주소" alt="대체문자열">
  ```

  - src 속성 : 이미지가 저장된 주소의 url 주소를 명시

  - alt 속성 : 이미지가 로딩될 수  없는 상황에서 이미지 대신 나타날 문자열 설정

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

- width 속성과 height 속성을 이용하면, 이미지의 너비와 높이를 각각 픽셀(pixel) 단위로 설정

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
  		<img src="/examples/images/img_flag.png" alt="flag" style="width:320px; height:214px; border: 1px solid black">
  	</a>
  	<p>이미지를 클릭해 보세요!</p>
  
  </body>
  
  </html>
  ```

#### 이미지 맵 만들기

- HTML에서는 <map>태그를 이용하여 이미지 맵(image map)을 제작

- 이미지 맵(image map)이란 이미지의 일부를 클릭할 수 있도록 만들어서 버튼처럼 사용하는 기능을 의미

- <img>태그의 usemap 속성을 <map>태그의 name 속성과 연결하면 이미지와 맵사이의 관계가 설정

- HTML <map>태그는 하나 이상의 <area>태그를 가지며, 이 <area>태그가 바로 버튼과 같은 역할

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
  	<meta charset="UTF-8">
  	<title>HTML Images</title>
  </head>
  
  <body>
  
  	<h1>이미지 맵 만들기</h1>
  	<img src="/examples/images/img_imagemap.jpg" alt="진실혹은거짓" usemap="#vending" style="width:320px; height:240px" />
  	<map name="vending"> 
  		<area  shape="rect" coords="90,60,180,130" alt="거짓" href="https://ko.wikipedia.org/wiki/%EA%B1%B0%EC%A7%93%EB%A7%90">
  		<area  shape="rect" coords="210,200,70,130" alt="진실" href="https://ko.wikipedia.org/wiki/%EC%A7%84%EC%8B%A4">
  	</map>
  	<p>표지판을 눌러보세요!</p>
  
  </body>
  
  </html>
  ```

  

