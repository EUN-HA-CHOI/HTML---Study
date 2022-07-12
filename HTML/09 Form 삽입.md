## 폼 삽입하기  
### 웹에서 만나는 폼  
:아이디,비밀번호 입력,로그인버튼 등 사용자가 웹 사이트로 정보를 보낼 수 있는 요소들.

### 폼을 만드는 form 태그  
```html
기본형 -> <form [속성="속성값"]>여러 폼 요소</form>. 
```
* 폼 태그의 속성  

| 종류 |                  설명                                 |
|-----|------------------------------------------------------|
|method|사용자가 입력한 내용을 서버 쪽 프로그램으로 어떻게 넘겨줄 것인지 지정|
|name|자바스크립트로 폼을 제어할 때 사용할 폼의 이름을 지정|
|action|<form> 태그 안의 내용을 처리해 줄 서버 프로그램 지정|
|target|action 속성에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에서 열도록 함|. 
  

```html
*입력한 폼 서버로 보내기
 <form action="000.php"> </form>  

*자동 완성 기능 autocomplate 속성  
*자동 완성 기능 끄기  
 <form action="000.php"autocomplate="off" > </form>  

### 폼 요소를 그룹으로 묶는 fieldset , legend 태그  
```html
  기본형 -> <fieldset [속성="속성값"]></fieldset>

  기본형 -> <fieldset>
             <legend>그룹 이름</legend>
          </fieldset>
```  

 
### 폼 요소에 레이블을 붙이는 lable 태그
``` html
기본형 -> <lable>레이블명<input></lable>
```

* 사용자가 아이디를 입력하는 폼 요소의 id 속성값을 <lable> 태그의 for 속성에게 알려주기 
```html 
기본형 -> <lable for="id"명>레이블명<input id="id명"></lable>
```

* 예시

``` html
<head>
  <meta charset="UTF-8">
  <title>레드향 주문하기</title>
</head>
<body>
  <h1>레드향 주문하기</h1>
  <form action="">
    <fieldset>
      <legend>상품 선택</legend>
      
    </fieldset>
    <fieldset>
      <legend>배송 정보</legend>  
    </fieldset>   
    
    <label>요청 사항<input></label>
  </form>
</body>
```
 <img width="486" alt="스크린샷 2022-05-23 오후 3 28 12" src="https://user-images.githubusercontent.com/97012561/169757027-3e5e8b41-b097-4f8d-85fe-15fafe3c2dae.png">



  
```html
<!-- 네이버 로그인 -->
<body>
  <h1><a href="#">NAVER</a></h1>
  <form action="/" method="post">
    <fieldset>
      <legend>로그인</legend>
      <ol>
        <li>
          <label for="userId">아이디</label>
          <input type="text"  id="userId" placeholder="아이디를 입력하세요." required autofocus />
        </li>
        <li>
          <label for="userPw">비밀번호</label>
          <input type="password" id="userPw" placeholder="비밀번호를 입력하세요." required />
        </li>
        <li>
          <input type="submit" value="로그인" />
        </li>
      </ol>
      <ul>
        <li><a href="#">비밀번호 찾기</a></li>
        <li><a href="#">아이디 찾기</a></li>
        <li><a href="#">회원가입</a></li>
      </ul>
    </fieldset>

  </form>
</body>
```

<img width="468" alt="스크린샷 2022-07-12 오후 11 41 56" src="https://user-images.githubusercontent.com/97012561/178517364-3a219190-a2ad-4a5d-9b84-b4947ab32df5.png">


```html
<!-- form 검색  -->
<body>
  <form action="/" method="post">
    <fieldset>
      <legend>자료검색영역</legend>
      <label for="srch">자료검색</label>
      <input type="search" id="srch" />
      <input type="image" src="images/btn_search.gif" alt="검색" />
    </fieldset>
  </form>
</body>
```
  
<img width="320" alt="스크린샷 2022-07-12 오후 11 43 56" src="https://user-images.githubusercontent.com/97012561/178517776-418a9791-c4e3-48d3-96e0-c813066e3b5f.png">

