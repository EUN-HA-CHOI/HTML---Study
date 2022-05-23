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







