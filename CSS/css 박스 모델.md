## 레이아웃을 구성하는 CSS 박스 모델  
* CSS와 박스 모델  
  -웹 문서의 내용을 박스 형태로 정의하는 방법  
  -박스 모델에는 마진과 패딩, 테두리 등 박스가 여러 겹 들어 있다.   
  -CSS에서 자주 사용하므로 잘 기억해 두어야 한다.  

* 블록 레벨 요소 block-level.  
  -블록 레벨은 태그를 사용해 요소를 삽입했을 때 혼자 한 줄을 차지하는 것.(=해당 요소 너비 100%)  
  -대표적인 태그로 `<h1>,<div>,<p>`.  
```html
<body>
  <h1>봄처럼 따뜻하고</h1>
  <div>여름처럼 <p class="accent">열정</p>적이며 </div>
  <p>가을처럼 아름답게 <br>물들어라 </p>	  
</body>
```
<img width="400" alt="스크린샷 2022-05-25 오후 8 24 01" src="https://user-images.githubusercontent.com/97012561/170251195-0c798992-43ef-4609-aeb5-478797d5e370.png">

* 인라인 레벨 요소 inline-level.  
  -콘텐츠 영역 만큼 차지하여 나머지 공간에는 다른 요소가 올 수 있다.  
  -한 줄에 인라인 레벨 요소를 여러 개 표시 가능.  
  -`<span>,<img><strong>`.  
```html
<body>
		<h1>봄처럼 따뜻하고</h1>
		<div>여름처럼 <span class="accent">열정</span>>적이며 </div>
		<p>가을처럼 아름답게 <br>물들어라 </p>	  
</body>
```
<img width="400" alt="스크린샷 2022-05-25 오후 8 30 08" src="https://user-images.githubusercontent.com/97012561/170252250-b4fc9c61-7b72-4835-96a8-d32ff34245fa.png">

* 박스 모델의 기본 구성  
  * 콘텐츠 영역
  * 박스와 콘텐츠 영역 사이의 여백인 패딩(padding)
  * 박스의 테두리(border)
  * 여러 박스 모델 사이의 여백인 마진(margin)
  * 마진과 패딩은 웹 문서에서 다른 콘텐츠 사이의 간격이나 배치 등을 고려할 때 필요함.  

* 콘텐츠 영역의 크기를 지정하는 width , height 속성   
 
|   종류  |                 설명                                 |  
|--------|-----------------------------------------------------|  
|  <크기> |너비나 높이의 값을 px나 em단위로 지정                        |  
| <백분율> |박스 모델을 포함하는 부모요소를 기준으로 너빗값이나 높잇갓을 %로 지정|


```css
<style>
    div {
      border:2px solid #000;
      margin-bottom: 20px;
    }
    .box1 {
      width:400px;
       height:100px;
    }
    .box2 {
      width:50%;
      height:100px;
    }
</style>
```
* 첫 번째 박스 크기는 웹 브라우저의 크기와 상관없이 유지.  

<img width="400" alt="스크린샷 2022-05-25 오후 8 50 30" src="https://user-images.githubusercontent.com/97012561/170255473-9a55cebe-6ef3-47d3-82e0-5a2d971ffc86.png">
 
* 두 번째 박스는 부모 요소인 body , 즉 웹 브라우저의 크기에 따라 달라짐.  

<img width="400" alt="스크린샷 2022-05-25 오후 8 51 06" src="https://user-images.githubusercontent.com/97012561/170255595-c72abc71-81a4-49cb-8310-08e26da03605.png">



* 박스 모델의 크기를 계산하는 box-sizing 속성  
  -박스 모델의 너비와 높이를 결정 
  -border-box : 테두리까지 포함해서 너빗값을 지정  
  -content-box : 콘텐츠 영역만 너빗값을 지정. 기본값    

##### ex.콘텐츠 영역 너비 200px , 콘텐츠와 테두리 사이 여백 20px , 테두리 두깨 10px 실제 박스 모델의 너비는?
```css
.box1 {
   width:200px;
   height:100px;
   padding:20px;
   border:10px solid #ccc;
}
```

##### 아래 그림의 실제 박스 모델의 값을 모두 더하면 260px   

<img width="213" alt="스크린샷 2022-05-25 오후 9 31 35" src="https://user-images.githubusercontent.com/97012561/170262519-0dd9e6fe-6dd6-451a-85d4-0b6d6343068a.png">  

```css
.box2 {
   box-sizing: border-box;
   width:200px;
   height:100px;
   padding:20px;
   border:10px solid #00f;
}
``` 
##### 아래 그림에서 box-sizing: border-box; 속성을 추가하면 실제 콘텐츠 영역의 너비인 140px 값이 나온다.  

<img width="220" alt="스크린샷 2022-05-25 오후 9 33 46" src="https://user-images.githubusercontent.com/97012561/170262928-b4fc3379-4b5f-4c4e-a930-4f96da6f247e.png">  


* 박스 모델에 그림자 효과를 주는 box-shadow 속성  
  -이미지의 그림자 위치나 색상,흐림 등을 지정  
  -`box-shadow: <수평 거리> <수직 거리> <흐림 정도> <번짐 정도> <색상> inset`  
  -수평거리와 수직 거리 반드시 지정하기(그림자 위치는 거리 값에 따라 움직임  


  




