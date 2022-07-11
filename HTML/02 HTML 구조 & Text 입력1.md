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
<h1> heading h1 큰 제목 </h1>
<!-- hr 구분선, / 는 종료한다는 태그
  p 문단 , br 줄바꿈 , &nbsp; 띄어쓰기 q 인용구, strong 강한 강조
 -->

 <p>장애에 &nbsp; &nbsp; &nbsp; 구애 없이 모든 사람들이 <br />
    손쉽게 정보를 공유할 수 있는<br />
    인터넷 공간 만들기


 <p>월드 와이드 웹 (World Wide Web)을 창시한 <strong>팀 버너스 리(Tim Berners-Lee)</strong>는 웹이란<br />
     <q>장애에 구애 없이 모든 사람들이 손쉽게 정보를 공유할 수 있는 공간</q>이라고 정의하였으며,<br />
     웹 콘텐츠를 제작할 때에는 장애에 구애됨이 없이 누구나 접근할 수 있도록 제작하여야<br />
     한다고 하였다. 이렇듯 웹 창시자가 웹의 기본적 철학에서 웹 접근성 부문을 강조함에도 불구하고,<br />
     웹 접근성을 바라보는 입장에 따라 다르게 정의하고 있다.<br />
</p>

```  
![image](https://user-images.githubusercontent.com/97012561/178235753-71516477-24ce-4218-90ae-fa599557b41c.png)
![image](https://user-images.githubusercontent.com/97012561/178236211-bc58bbc0-7d41-4923-b0fa-bb8604d0e56c.png)

```html
 <!-- blockquote 인용문 em 약한 강조 -->
 <blockquote>
    <p>웹의 힘은 그것의 보편성에 있다. 장애에 구애없이 모든 사람이 접근할 수 있는 것이 필수적인 요소이다.</p>

    <p><em>팀 버너스 리 경 - 웹의 창시자 (Tim Berners - Lee , W3C Director and inventor of the World Wide Web)</em></p>
</blockquote>
```

```html
<!-- address 사이트 정보, 주소, 연락처 -->
<address>대구광역시 동구 첨단로 53 (41068) 한국지능정보사회진흥원 디지털포용본부 ☎ 053-230-1388</address>
<p>Copyright ⓒ 2017 National Information Society Agency</p>

<!-- > , &gt; , < ,  &lt; & , &amp; -->
<p>HOME &gt;  웹 접근성이란 &gt; 웹 접근성 개요</p>
<p>HOME &lt;  웹 접근성이란 &lt; 웹 접근성 개요</p>
<p>HOME &amp; 웹 접근성이란 &amp; 웹 접근성 개요</p>
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
