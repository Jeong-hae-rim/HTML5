# CSS

## 1. CSS 기초

### CSS란?

- CSS는 Cascading Style Sheets의 약자
- CSS는 HTML 요소들이 각종 미디어에서 어떻게 보이는가를 정의하는 데에 사용되는 스타일 시트 언어
- HTML4부터는 이러한 모든 서식 설정을 HTML 문서로부터 따로 분리하는 것이 가능해짐
- 오늘날 대부분의 웹 브라우저들은 모두 CSS를 지원함

### CSS를 사용하는 이유

- HTML만으로 웹페이지르 제작할 경우 HTML 요소의 세부 스타일을 일일히 따로 지정해줘야만 함
- 이 작업은 매우 많은 시간이 걸리며 완성한 후에도 스타일의 변경 및 유지 보수가 매우 힘들어짐
- 이 문제점을 해소하기 위해 W3C에서 만든 스타일 시트 언어가 CSS
- CSS는 웹 페이지의 스타일을 별도의 파일로 저장할 수 있게 해주므로 사이트 전체 스타일을 손쉽게 제어
- 또한 웹 사이트의 스타일을 일관성 있게 유지해주며, 그에 따른 유지보수도 쉬워짐
- 외부 스타일 시트는 보통 확장자를 .css 파일로 저장

## 2. CSS 문법

### CSS 문법

![CSS 문법](http://tcpschool.com/lectures/img_css_syntax.png)

- CSS 문법은 선택자(selector)와 선언부(declaratives)로 구성
- 선택자는 CSS를 적용하고자 하는 HTML 요소(element)를 가리킨다.
- 선언부는 하나 이상의 선언들을 세미콜론(;)으로 구분하여 포함
- 중괄호({ })를 사용해 전체를 둘러쌈
- 각 선언은 CSS 속성명(property)과 속성값(value)을 가지며, 그 둘은 콜론(:)으로 연결된다.
- 이러한 CSS 선언(declaration)은 언제나 마지막에 세미콜론(;)으로 끝마침

### CSS 선택자

스타일을 적용할 HTML 요소를 가리키는 데 사용하는 선택자는 다음과 같다.

#### HTML 요소 선택자

- CSS를 적용할 대상으로 HTML 요소의 이름을 직접 사용하여 선택

  ```css
  	<style>
  		h2 {
  			color: teal;
  			text-decoration: underline;
  		}
  	</style>
  ```

#### 아이디(id) 선택자

- 아이디 선택자는 CSS를 적용할 대상으로 특정 요소를 선택할 때 사용

- 선택자는 웹 페이지에 포함된 여러 요소 중에서 특정 아이디 이름을 가지는 요소만을 선택

  ```css
  <style>
      #heading {
          color: teal;
          text-decoration: line-through;
      }
  </style>
  ```

- HTML과 CSS에서는 하나의 웹 페이지에 속하는 여러 요소에 같은 아이디 이름을 사용해도 별 문제 없이 동작

- 이렇게 중복된 아이디를 가지고 자바스크립트 작업을 하게 되면 오류 발생

- 되도록이면 하나의 웹 페이지에 속하는 요소에는 다른 아이디 이름을 사용하거나 클래스를 사용하는 것이 좋음

#### 클래스(Class) 선택자

- 클래스 선택자는 특정 집단의 여러 요소를 한 번에 선택할 때 사용

- 이런 특정 집단을 클래스(class)라고 하며, 같은 클래스 이름을 가지도 요소들을 모두 선택

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>CSS Syntax</title>
  	<style>
  		.headings {
  			color: lime;
  			text-decoration: overline;
  		}
  	</style>
  </head>
  <body>
  
  	<h1>클래스 선택자를 이용한 선택</h1>
  	<h2 class="headings">이 부분에 스타일을 적용합니다.</h2>
  	<p>클래스 선택자를 이용하여 스타일을 적용할 HTML 요소들을 한 번에 선택할 수 있습니다.</p>
  	<h3 class="headings">이 부분에도 같은 스타일을 적용합니다.</h3>
  
  </body>
  </html>
  ```

#### 그룹(group) 선택자

- 그룹 선택자는 위에서 언급한 여러 선택자를 같이 사용하고자 할 때 사용

- 그룹 선택자는 여러 선택자를 쉼표 (, )로 구분하여 연결

- 이런 그룹 선택자는 코드를 중복해서 작성하지 않도록 해 코드를 간결하게 만들어줌

  ```css
  <style>
      h1 { color: navy; }
      h1, h2 { text-align: center; }
      h1, h2, p { background-color: lightgray; }
  </style>
  ```

### CSS 주석(comments)

- 주석(comments)이란 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미

- 다른 CSS 코드와는 달리 웹 브라우저에 의해 해석되지 않음

- CSS에서 주석을 표현하는 방법

  ```css
  /* 주석내용 */
  ```

  ```css
  <style>
  p { color: teal; /*이것은 한 줄짜리 주석입니다.*/ font-size: 30px; }
  /* 
  
  이것은 두 줄짜리 주석입니다.
  
  몇 줄이라도 가능합니다. 
  
  */
  </style>
  ```

- CSS에서 주석을 작성할 때는 절대로 주석 내부에 또 다른 주석을 넣어서는 안 된다.

  ```css
  /*
  
  첫 번째 주석의 첫 번째 라인입니다. /* 두 번째 주석입니다. */
  
  첫 번째 주석의 두 번째 라인입니다.
  
  */
  ```

## 3. CSS 적용

### CSS를 적용하는 방법

- HTML 문서에 CSS 스타일을 적용할 때는 다음과 같은 세 가지 방법을 사용

  1.  인라인 스타일(Inline style)

     - 인라인 스타일이란 HTML 요소 내부에 style 속성을 사용하여 CSS 스타일을 적용하는 방법

     - 이러한 인라인 스타일은 해당 요소에만 스타일을 적용

       ```css
       <body>
           <h2 style="color:green; text-decoration:underline">
               인라인 스타일을 이용하여 스타일을 적용하였습니다.
           </h2>
       </body>
       ```

     - 이 방식은 한 번 설정된 스타일을 변경하기가 매우 어려우며, 스타일 시트를 사용하는 많은 이점을 잃게 됨

     - 따라서 이 방식은 될 수 있으면 꼭 필요한 경우에만 사용

  2. 내부 스타일 시트(Internal style sheet)

     - 내부 스타일 시트를 이용하는 방법은 HTML 문서 내의 <head>태그에 <style>태그를 사용하여 CSS 스타일을 적용

     - 이러한 내부 스타일 시트는 해당 HTML 문서에만 스타일을 적용

       ```css
       <head>
           <style>
               body { background-color: lightyellow; }
               h2 { color: red; text-decoration: underline; }
           </style>
       </head>
       ```

  3. 외부 스타일 시트(External style sheet)

     - 외부 스타일 시트를 이용하는 방법은 웹 사이트 전체의 스타일을 하나의 파일에서 변경할 수 있도록 해줌

     - 외부에 작성된 이러한 스타일 시트 파일은 .css 확장자를 사용하여 저장

     - 스타일을 적용할 웹 페이지의 <head>태그에 <link>태그를 사용하여 외부 스타일 시트를 포함해야만 스타일이 적용

       ```css
       <head>
           <link rel="stylesheet" href="/examples/media/expand_style.css">
       </head>
       ```

       - 위의 예제에서 사용된 CSS 파일의 내용

         ```css
         body { background-color: lightyellow; }
         p { color: red; text-decoration: underline; }
         ```

### 스타일 적용의 우선 순위

- 위에서 설명한 스타일 적용 방법들이 혼합되어 사용될 경우, 최종적으로 적용되는 스타일은 다음 순서에 따라 결정

  1. 인라인 스타일 (HTML 요소 내부에 위치함)
  2. 내부 / 외부 스타일 시트 (HTML 문서의 head 요소 내부에 위치함)
  3. 웹 브라우저 기본 스타일

- 예를 들어 인라인 스타일이 적용된 태그는 내부나 외부 스타일 시트와는 상관없이 무조건 인라인 스타일이 적

- 또한, 내부 스타일 시트와 외부 스타일 시트는 가장 마지막에 적용된 스타일 시트가 적용

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  <head>
  	<meta charset="UTF-8">
  	<title>CSS Apply</title>
  	<link rel="stylesheet" href="/examples/media/tcpschool_expand_style.css">
  </head>
  <body>
  	<h2>이 부분은 외부 스타일 시트만이 적용됩니다.</h2>
  	<h2 style="color:maroon; text-decoration:line-through">
  		이 부분은 인라인 스타일과 외부 스타일 시트가 둘 다 적용됩니다.
  	</h2>
  </body>
  </html>
  ```

- 따라서 웹 사이트의 스타일 적용은 외부 스타일 시트를 사용하는 것이 유지 보수도 편하며, 가장 안정적

## 4. CSS 기본 속성

### 1. 색

- CSS에서 색을 표현하는 방법에는 다음과 같이 세 가지 방법이 있습니다. 

  1. 색상 이름으로 표현

     - W3C에서 정의한 16개의 HTML4 표준 색상 이름

       ![image](https://user-images.githubusercontent.com/58800295/88020209-41d80400-cb66-11ea-97c8-a001646e10da.png)

     - HTML에서 색상 이름은 대소문자를 구분하지 않습니다.

     ```css
     <style>
         .blue { color: blue; }
         .green { color: green; }
         .silver { color: silver; }
     </style>
     ```

  2. RGB 색상값으로 표현

     - 모니터나 스크린은 빨간색(Red), 녹색(Green), 파란색(Blue)을 혼합하여 색을 표현

     - 따라서 HTML에서도 이 세 가지 색을 가지고 색을 표현하는 RGB 색상을 사용

     - RGB 색상의 기본색(Red, Green, Blue)은 각각 0부터 255까지의 범위

       ```css
       <style>
           .blue { color: rgb(0,0,255); }
           .green { color: rgb(0,128,0); }
           .silver { color: rgb(192,192,192); }
       </style>
       ```

  3. 16진수 색상값으로 표현

     - 16진수 색상값은 RGB 색상값을 각각 16진수로 변환한 것

     - 따라서 RGB 색상의 기본색(Red, Green, Blue)은 각각 00부터 FF까지의 범위

     - 예를 들면, 녹색을 나타내는 RGB 색상값 rgb(0,255,0)은 16진수 색상값으로는 #00FF00이 됨

       ```scss
       <style>
           .blue { color: #0000FF; }
           .green { color: #008000; }
           .silver { color: #C0C0C0; }
       </style>
       ```

### 2. 배경

- CSS에서 사용할 수 있는 background 속성은 다음과 같다.

  1. background-color

     - background-color 속성은 해당 HTML 요소의 배경색(background color)을 설정

       ```css
       <style>
           body { background-color: lightblue; }
           h1 { background-color: rgb(255,128,0); }
           p { background-color: #FFFFCC; }
       </style>
       ```

  2. background-image

     - background-image 속성은 해당 HTML 요소의 배경으로 나타날 배경 이미지(image)를 설정

     - 설정된 배경 이미지는 기본 설정으로 HTML 요소 전체에 걸쳐 반복되어 나타남

       ```css
       <style>
           body { background-image: url("/examples/images/img_background_good.png"); }
       </style>
       ```

     - 배경 이미지를 사용할 때에는 이미지가 본문의 텍스트를 방해하지 않도록 주의를 기울여야 함

       ```css
       <style>
           body { background-image: url("/examples/images/img_background_bad.png"); }
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88021250-20781780-cb68-11ea-943c-6203f8d500e9.png)

  3. background-repeat

     - 배경 이미지는 기본 설정으로 수평과 수직 방향으로 모두 반복되어 나타남

     - background-repeat 속성을 이용하면 이러한 배경 이미지를 수평이나 수직 방향으로만 반복되도록 설정

     - 배경 이미지의 수평 반복

       ```css
       <style>
           body { background-image: url("/examples/images/img_man.png"); background-repeat: repeat-x; }
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88021352-4b626b80-cb68-11ea-832a-7e9016591f61.png)

     - 배경 이미지의 수직 반복

       ```css
       <style>
       
           body { background-image: url("/examples/images/img_man.png"); background-repeat: repeat-y; }
       
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88021426-659c4980-cb68-11ea-9fab-7b644d09e2a4.png)

     - 배경 이미지가 반복되지 않고 한 번만

       ```css
       <style>
           body { background-image: url("/examples/images/img_man.png"); background-repeat: no-repeat; }
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88021507-8b295300-cb68-11ea-822a-05590e9d43d7.png)
       

  4. background-position

     - background-position 속성은 반복되지 않는 배경 이미지의 상대 위치(relative position)를 설정

       ```css
       <style>
           body {
               background-image: url("/examples/images/img_man.png");
               background-repeat: no-repeat;
               background-position: top right;
           }
       </style>
       ```

     - 이 속성에서 사용할 수 있는 키워드의 조합

       1. left top

       2. left center

       3. left bottom

       4. right top

       5. right center

       6. right bottom

       7. center top

       8. center center

       9. center bottom

     - 또한, 퍼센트(%)나 픽셀(px)을 사용하여 상대 위치를 직접 명시

     - 이때 상대 위치를 결정하는 기준은 해당 요소의 왼쪽 상단(left top)

       ```html
       <style>
           body {
               background-image: url("/examples/images/img_man.png");
               background-repeat: no-repeat;
               background-position: 100px 200px;
           }
       </style>
       ```

  5. background-attachment

     - background-attachment 속성을 사용하여 위치가 설정된 배경 이미지를 해당 위치에 고정시킴

     - 이렇게 고정된 배경 이미지는 스크롤과는 무관하게 화면의 위치에서 이동하지 않음

       ```css
       <style>
           body {
               background-image: url("/examples/images/img_man.png");
               background-repeat: no-repeat;
               background-position: left bottom;
               background-attachment: fixed;
           }
       </style>
       ```

  - #### background 속성 한 번에 적용하기

    - 위에서 언급한 모든 background 속성을 이용한 스타일을 한 줄에 설정

      ```css
      <style>
          body { background: #FFCCCC url("/examples/images/img_man.png") no-repeat left bottom fixed; }
      </style>
      ```

  - CSS background 속성

    |         속성          |                             설명                             |
    | :-------------------: | :----------------------------------------------------------: |
    |      background       | 모든 background 속성을 이용한 스타일을 한 줄에 설정할 수 있음. |
    |   background-color    |                 HTML 요소의 배경색을 설정함.                 |
    |   background-image    |              HTML 요소의 배경 이미지를 설정함.               |
    |   background-repeat   |           설정된 배경 이미지의 반복 유무를 설정함.           |
    |  background-position  |       반복되지 않는 배경 이미지의 상대 위치를 설정함.        |
    | background-attachment |   배경 이미지를 스크롤과는 무관하게 해당 위치에 고정시킴.    |

### 3. 텍스트

- CSS에서 사용할 수 있는 대표적인 text 속성은 다음과 같습니다.

  1. color

     - color 속성은 텍스트의 색상을 설정
     - 웹 페이지에서 텍스트의 기본 색상은 검정색
     - &lt;body&gt; 태그에 명시된 color 속성값은 웹 페이지 내의 모든 텍스트 요소에 적용
     - 각 요소별로 따로 명시된 color 속성값이 있다면, 해당 속성값이 &lt;body&gt;태그에 명시된 속성값보다 우선 적용

     ```css
     <style>
         body { color: red; }
         p { color: maroon; }
     </style>
     ```

  2. direction

     - direction 속성은 텍스트가 써지는 방향을 설정

     - 웹 페이지에서 텍스트는 기본적으로 왼쪽에서 오른쪽 방향으로 써짐

     - direction 속성이 left-to-right(ltr)일 때는 기본 설정처럼 텍스트가 왼쪽에서 오른쪽 방향으로 써짐

     - direction 속성이 right-to-left(rtl)일 때는 텍스트가 반대 방향인 오른쪽에서 왼쪽 방향으로 써짐

     - 다음 예제는 "객체 지향 프로그래밍"이라는 문자열을 한글과 아랍어로 각각 나타낸 예제

       ```css
       <style>
           .rightToLeft { direction: rtl; }
       </style>
       ```

       ![image-20200721155048655](C:\Users\Jeong Hae Rim\AppData\Roaming\Typora\typora-user-images\image-20200721155048655.png)

       - 아랍어는 한글이나 영어와는 달리 오른쪽에서 왼쪽 방향으로 텍스트를 읽고 쓰는 언어
       - 따라서 아랍어와 같이 텍스트를 반대 방향으로 쓰는 언어를 나타낼 때는 텍스트가 써지는 방향을 direction 속성을 사용하여 변경

  3. letter-spacing

     - letter-spacing 속성은 텍스트 내에서 글자 사이의 간격을 설정

       ```css
       <style>
           .decLetterSpacing { letter-spacing: -3px; }
           .incLetterSpacing { letter-spacing: 10px; }
       </style>
       ```

  4. word-spacing

     - word-spacing 속성은 텍스트 내에서 단어 사이의 간격을 설정

     - letter-spacing 속성과는 달리 문자 간의 간격이 아닌 단어 간의 간격을 기준으로 설정

       ```css
       <style>
           .decWordSpacing { word-spacing: -3px; }
           .incWordSpacing { word-spacing: 10px; }
       </style>
       ```

  5. text-indent

     - text-indent 속성은 단락의 첫 줄에 들여쓰기할지 안 할지를 설정

     - 웹 페이지에서 단락은 기본적으로 들여쓰기가 설정되어 있지 않음

       ```css
       <style>
           .paraIndent { text-indent: 30px; }
       </style>
       ```

       

  6. text-align

     - text-align 속성은 텍스트의 수평 방향 정렬을 설정

     - text-align 속성으로 설정된 정렬 방향은 text-direction 속성과는 상관없이 우선적으로 적용

       ```css
       <style>
           h2 { text-align: left; }
           h3 { text-align: right; }
           h4 { text-align: center; }
       </style>
       ```

  7. text-decoration

     - text-decoration 속성은 텍스트에 여러 가지 효과를 설정하거나 제거하는데 사용

     - text-decoration 속성값을 none으로 설정하여 링크(link)가 설정된 텍스트의 밑줄을 제거하는데 자주 사용

       ```css
       <style>
           h2 { text-decoration: overline; }
           h3 { text-decoration: line-through; }
           h4 { text-decoration: underline; }
           a { text-decoration: none; }
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88778149-1dfa6b00-d1c3-11ea-912a-40c65065ca74.png)

  8. text-transform

     - text-transform 속성은 텍스트에 포함된 영문자에 대한 대소문자를 설정

     - 이 속성은 텍스트에 포함된 모든 영문자를 대문자나 소문자로 변경

     - 또한, 단어의 첫 문자만을 대문자로 변경시킬 수도 있음

     - text-transform 속성은 한글에는 영향을 주지 않으며, 오직 영문자에만 적용

       ```css
       <style>
           h2 { text-transform: uppercase; }
           h3 { text-transform: lowercase; }
           h4 { text-transform: capitalize; }
       </style>
       ```

       ![image](https://user-images.githubusercontent.com/58800295/88778322-59953500-d1c3-11ea-8bf6-46a3cc62851f.png)

  9. line-height

     - line-height 속성은 텍스트의 줄 간격을 설정

       ```css
       <style>
           .narrowLineHeight { line-height: 0.8; }
           .wideLineHeight { line-height: 1.8; }
       </style>
       ```

  10. text-shadow

      - text-shadow 속성은 텍스트에 간단한 그림자 효과를 설정

        ```css
        <style>
            h2 { text-shadow: 2px 1px #3399CC; }
        </style>
        ```

  11. CSS text 속성

      |      속성       |                             설명                             |
      | :-------------: | :----------------------------------------------------------: |
      |      color      |                   텍스트의 색상을 설정함.                    |
      |    direction    |                텍스트가 쓰이는 방향을 설정함.                |
      | letter-spacing  |           텍스트 내에서 문자 사이의 간격을 설정함.           |
      |  word-spacing   |           텍스트 내에서 단어 사이의 간격을 설정함.           |
      |   text-indent   |        단락의 첫 줄을 들여쓰기할지 안 할지를 설정함.         |
      |   text-align    |              텍스트의 수평 방향 정렬을 설정함.               |
      | text-decoration |         텍스트에 여러 가지 효과를 설정하거나 제거함.         |
      | text-transform  |       텍스트에 포함된 영문자에 대한 대소문자를 설정함.       |
      |   line-height   |                  텍스트의 줄 간격을 설정함.                  |
      |   text-shadow   |                텍스트에 그림자 효과를 설정함.                |
      |  unicode-bidi   | direction 속성과 같이 사용하여 텍스트의 기본 출력 방향을 설정함. |
      | vertical-align  |           HTML 요소 내의 수직 방향 정렬을 설정함.            |
      |   white-space   |                HTML 요소 내의 여백을 설정함.                 |

### 4.  글꼴

- CSS에서 사용할 수 있는 font 속성은 다음과 같다.

  1. font-family

     - CSS에는 두 가지의 글꼴 집합이 존재한다.

       - generic family : 비슷한 모양을 가지는 글꼴 집합 ("Serif", "Monospace" 등)

       - font family : 특정 글꼴 집합 ("Times", "Courier" 등)

     - font-family 속성은 하나의 글꼴만을 설정할 수도 있고, 여러 개의 글꼴을 같이 설정할 수도 있음

     - font-family 속성 값이 여러 개의 글꼴로 설정되어 있으면, 웹 브라우저는 위에서부터 순서대로 글꼴을 읽어들임

     - 만약 사용자의 컴퓨터에 첫 번째로 읽어들인 글꼴이 없으면 다음 글꼴을 확인

     - 이런 방식으로 계속해서 읽어 들인 글꼴이 존재하는지를 확인하여, 읽어 들인 글꼴이 사용자의 컴퓨터에 존재하면 해당 글꼴로 표시

     - 글꼴의 이름이 한 단어 이상으로 이루어지면 반드시 따옴표를 사용하여 둘러 쌓아야 함

     - 또한, 여러 개의 글꼴을 나열할 때에는 쉼표(,)로 구분

       ```css
       <style>
           .serif { font-family: "Times New Roman", Times, serif; }
           .sansserif { font-family: Arial, Helvetica, sans-serif; }
       </style>
       ```

  2. font-style

     - font-style 속성은 주로 이탤릭체를 사용하기 위해 사용하며, 다음과 같이 3가지의 속성값을 가짐

       - normal : 텍스트에 어떠한 스타일도 적용하지 않음

       - italic : 텍스트를 이탤릭체로 나타냄.

       - oblique : 텍스트를 기울임. (italic과 매우 유사하지만 지원하는 웹 브라우저가 거의 없음)

         ```css
         <style>
             .normal { font-style: normal; }
             .italic { font-style: italic; }
             .oblique { font-style: oblique; }
         </style>
         ```

  3. font-variant

     - font-variant 속성은 속성값이 small-caps로 설정되면, 텍스트에 포함된 영문자 중 모든 소문자를 작은 대문자(small-caps) 글꼴로 변경

     - 이때 영문자 중 대문자는 기존 크기 그대로 출력

     - 작은 대문자(small-caps) 글꼴이란 텍스트의 기존 대문자보다는 약간 작은 크기의 대문자를 의미

     - font-variant 속성은 한글에는 적용되지 않으며, 영문자에만 적용

       ```css
       <style>
           .normal { font-variant: normal; }
           .smallCaps { font-variant: small-caps; }
       </style>
       ```

  4. font-weight

     - font-weight 속성은 텍스트를 얼마나 두껍게 표현할지를 설정

     - 사용할 수 있는 속성값에는 lighter, normal, bold, bolder 등이 있음

     - 또한, 100, 200, 300, ... , 900 등과 같이 숫자로 텍스트의 두께를 설정 가능

       ```css
       <style>
           .normal { font-weight: normal; }
           .bold { font-weight: 600; }
           .bolder { font-weight: bolder; }
       </style>
       ```

  5. font-size

     - font-size 속성은 텍스트의 크기를 설정

     - 웹 디자인에서 텍스트의 크기는 매우 중요한 표현 요소

       - 하지만 제목을 표현하기 위해서는 텍스트의 크기만 키워서는 안 됨
       - 제목을 위한 HTML 요소인 <h1>태그부터 <h6>태그를 사용

     - font-size 속성값은 다음과 같이 두 가지 방식으로 표현

       1. 절대적 크기
          - 텍스트의 크기를 명시된 크기 그대로 설정하고자 할 때 사용
          - 절대적 크기로 설정된 텍스트는 모든 웹 브라우저에서 같은 크기로 표현
       2. 상대적 크기
          - 텍스트를 둘러싸고 있는 HTML 요소들의 크기에 따라 텍스트의 크기도 같이 변하는 방식
          - 사용자가 웹 브라우저를 통해 텍스트의 크기를 직접 변경 가능

     - font-size 속성값에 자주 사용되는 대표적인 크기 단위

       1. 백분율 단위(%)는 기본 크기를 100%로 놓고, 그에 대한 상대적인 크기를 설정
       2. 배수 단위(em)는 해당 글꼴(font)의 기본 크기를 1em으로 놓고, 그에 대한 상대적인 크기를 설정
          - 배수 단위(em)로 설정된 텍스트는 사용자가 웹 브라우저를 통해 크기를 재조정 가능
       3. 픽셀 단위(px)는 스크린의 픽셀(pixel)을 기준으로 하는 절대적인 크기를 설정

       ```css
       <style>
           body { font-size: 100%; }
           #large { font-size: 2.5em; }
           #small { font-size: 0.7em; }
           #fixed { font-size: 20px; }
       </style>
       ```

  6. CSS font 속성

     |     속성     |                             설명                             |
     | :----------: | :----------------------------------------------------------: |
     |     font     |   모든 font 속성을 이용한 스타일을 한 줄에 설정할 수 있음.   |
     | font-family  |          텍스트의 글꼴 집합(font family)을 설정함.           |
     |  font-style  |            주로 이탤릭체를 사용하기 위해 사용함.             |
     | font-variant | 텍스트에 포함된 영문자 중 소문자만을 작은 대문자(small-caps) 글꼴로 변경시킴. |
     | font-weight  |          텍스트를 얼마나 두껍게 표현할지를 설정함.           |
     |  font-size   |                   텍스트의 크기를 설정함.                    |

### 5. 링크



