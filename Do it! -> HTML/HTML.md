## 웹 개발 시작하기  
### 웹 개발 알아보기  
* 정적 사이트: 웹 브라우저 화면에 보이는 겉모습  
* 동적 사이트: 웹 브라우저 화면에 보이는 겉모습 안에 기능  
* 서버 : 서비스를 제공하는 객체  
* 클라이언트 : 서비스를 이용하는 객체  
#####  ->즉 , 서버는 판매자, 클라이언트는 구매자

#### - 프런트엔드 Frond-end -
* 웹 브라우저 화면에 보이는 부분을 다룸 -> 웹 사이트 제작  
* 기본영역 : HTML + CSS + Javascript + git , github 
* library : jQuery , D3.js, Bootstrap 등  
* Framework : React , Angular , Vue.js 등 

### 웹 개발의 기본 HTML + CSS + Javascript.
* 웹 문서의 뼈대를 만드는 HTML : 웹 브라우저 창에 웹 문서의 내용은 보여줌.  
* 웹 문서를 꾸미는 CSS : HTML로 만든 내용을 사용자가 알아보기 쉽게 꾸미거나 사용하기 편리하도록 배치할 때 사용.  
* 사용자 동작에 반응하는 Javascript : 단순히 내용을 보여주는 것에 그치지 않고 사용자가 클릭하거나 스크롤하는 동작에 따라 반응.  

## HTML 기본 문서 만들기  
### HTML이란 ?  
##### 웹 문서를 만드는 언어로  Hyper Text Markup Language 의 줄임말.  

* 웹 편집기에 입력한 태그  
```html 
<h1>제목</h1>  
<p>텍스트 단락</p>
<table>
  <tr>
    <td>셀1</td>
    <td>셀2</td>
  </tr>
  <tr>
    <td>셀3</td>
    <td>셀4</td>
  </tr>
</table>. 
```

* 웹 브라우저에 보이는 모습  

## 제목   

### 텍스트 단락 
|     |    |
|-----|----|
| 셀1 | 셀2 |  
| 셀3 | 셀4 |

### HTML 구조 파악하기  
* HTML 문서의 기본 구조 살펴보기  
``` HTML
<!DOCTYPE html>로 시작해 <html>,<head>,<body> 라는 3개의 영역으로 구성되어 있음.  

<!DOCTYPE html> : 현재 문서가 html5 언어로 작성한 웹 문서라는 뜻. 
<html> ~ </html> : 웹 문서의 시작과 끝. 
<head> ~ </head> : 문서의 정보를 저장.  
<body> ~ </body> : 웹 브라우저 화면에 나타나는 내용. HTML 태그는 <body>안에 속함.

<meta> : 웹 문서와 관련된 정보를 지정할 때 사용. 화면에 글자 표시할 때 어떠한 인코딩을 사용할지 지정함.
<meta charset="UTF-8"> : 한글로 된 내용을 표시할 때 사용.  
<title>문서 제목 <title>
```  

* HTML 파일 만들기
``` HTML
<!DOCTYPE html>
<html lang="ko">
 <head>
   <meta charset="UTF-8">
   <title>첫 번째 문서 연습</title>
 </head>
 <body>
   <h1>웹 문서 만들기</h1>
 </body>
</html>  
```

### 웹 문서 구조를 만드는 시맨틱 태그  
##### 시맨틱 태그 : 이름만 봐도 의미를 알 수 있음
##### 헤더 , 본문 , 푸터 영역으로 나누어지고 웹 사이트마다 한 두 영역 추가됨.  

* 시맨틱 태그를 사용하여 만든 웹 문서 
``` html 
<!--(..생략..)-->  
<div id="container">
  <header>                     <!--헤더 영역-->
    ....
    <nav>  <!--내비게이션 영역-->
    </nav>
  </header>
  <main class="contents">.      <!--본문 영역-->
    <section id="headling">
      <h2>몸과 마음이 치유되는 섬</h2>
      
    </section>
  </main>
  <footer>                     <!--푸터 영역-->
    <section id="bottomMenu">
      
    </section>
  </footer>
</div>
```  

* 웹 문서 구조를 만드는 주요 시맨틱 태그 
``` html 
-헤더 영역을 나타내는 <header> 태그  : 검색창이나 사이트 메뉴 삽입.
-내비게이션 영역을 나타내는 <nav> 태그 : 웹 문서 연결고리, 여러 개 사용할 경우 id 속성 지정하여 nav 마다 스타일 적용.
-핵심 콘텐츠를 담는 <main> 태그 : 웹 문서에서 한 번만 사용.
-독립적인 콘텐츠를 담는 <article> 태그 
-콘텐츠 영역을 나타내는 <section> 태그
-푸터 영역을 나타내는 <footer> 태그 : 웹 문서 맨 아래에 두고 다양한 정보 넣기
-여러 소스를 묶는 <div> 태그 : 구별할 때 사용 , <div id="header"> 나 <div class="detail"> 속성을 사용하여 꾸밈.
```

## 웹 문서에 다양한 내용 입력하기  
### 텍스트 입력하기 
``` html
제목을 나타내는 <hn>
텍스트 단락을 만드는 <p> 태그, 줄을 바꾸는 <br> 태그 (<br>태그는 단독으로 사용하여 닫는 태그 필요 없음)
인용할 때 쓰는 <blockquote> 태그
텍스트를 굵게 강조 하려면 <strong>, 굵게 표시할 <b> 태그
이탤릭체로 강조할 <em> ,이탤릭체로 표시할 <i> 태그
```

* 텍스트 태그 여러 개 삽입하기 예제  
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>탐라국 입춘굿</title>
  <link rel="stylesheet" href="css/poster.css">
</head>
<body>
  <div id="container">
    <h1>탐라국 입춘굿</h1>    
    <p>탐라국 입춘굿놀이는 전국적으로 유일하게 입춘날 벌어지는 축제이자 제주도의 문화축제 중에서 유일하게 전통시대부터 존재했던 축제이다.</p>
    <p>제주에서 입춘은 새철 드는 날. <br>
      신구간이 끝나 하늘의 1만8000신이 지상으로 내려와 새해 일들을 시작하는 때다.
    </p>
    <p>자세한 정보 보기</p>
    <h2>일정</h2>
    
    <h2>먹거리</h2>
  </div>
</body>
</html>
```

 * 결과 확인하기 



<img width="478" alt="스크린샷 2022-05-19 오후 2 29 41" src="https://user-images.githubusercontent.com/97012561/169217173-55d42248-d36f-4d35-af11-c6c060cd43d5.png">






