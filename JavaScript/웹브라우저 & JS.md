## 웹 브라우저와 자바스크립트가 만났을 때  
##### 웹 브라우저에는 자바스크립트 소스를 읽고 처리하는 해석기가 있다. 따라서 자바스크립트 소스는 웹 문서에서 `<scrip>` 태그를 이용해 작성.  

* 웹 문서 안에 <script> 태그로 자바스크립트 작성하기  
 -소스 코드가 짧으면 실행할 위치에 바로 `<scrip></scrip>` 코드를 작성 , 문서 안의 어디든 위치 가능 , 하나의 문서에서 여러 개 사용 가능  
 -이미지 텍스트 등 다 표시한 후 자바스크립트 실행. `</body>` 태그 직전에 자바스크립트 소스 삽입  
 :영어 대소문자 구별.  

``` javascript
<script>
	var heading = document.querySelector('#heading');
	heading.onclick = function() {
	heading.style.color = "red";
	}
</script>
```
<img width="180" alt="스크린샷 2022-06-27 오후 1 41 32" src="https://user-images.githubusercontent.com/97012561/175861416-87caee27-c0ec-402e-9ad9-22f12461281a.png">  <img width="200" alt="스크린샷 2022-06-27 오후 1 41 46" src="https://user-images.githubusercontent.com/97012561/175861430-4b28de62-b98f-45fc-bbe7-f530b6d9840a.png">

* 외부 스크립트 파일로 연결해서 자바스크립트 작성하기  
  -자바스크립트 소스를 따로 파일로 저장한 뒤 웹 문서와 연결하여 사용 외부 자바스크립트 파일은       
   `<script>` 태그 없이 소스만 작성 후 확장자는 `*.js`  
  -html 문서에서 `<script>` 태그의 src 속성을 이용해서 자바스크립트 파일 연결  
  -기본형 `<script src="외부 스크립트 파일 경로"></script>`.   

