## 이미지와 그러데이션 효과로 배경 꾸미기  

* 배경색을 지정하는 background-color 속성  
  -16진수나 rgb값 또는 색상 이름을 사용해서 지정한다.  

``` css
background-color: #00000;
background-color: rgb(0,128,0);
background-color: green;
```

* 배경색의 적용 범위를 조절하는 background-clip 속성  
  -박스 모델 관점에서 배경의 적용 범위를 조절
  
|      종류 |              설명                   |
|----------|------------------------------------|
|border-box|박스 모델의 가장 외곽인 테두리까지 적용. 기본값|
|padding-box|박스 모델의 테두리를 뺀 패딩 범위까지 적용|
|content-box|박스 모델에서 내용 부분에만 적용|

```css
#clip-border {
      background-clip: border-box;  /*테두리까지 배경 지정*/
    }
    #clip-padding {       /*테두리를 뺀 패딩 범위까지 배경 지정*/
      background-clip: padding-box;
    }
    #clip-content {       /*콘텐츠에만 배경 지정*/
      background-clip: content-box;
    }
```
<img width="200" alt="스크린샷 2022-06-01 오후 4 49 22" src="https://user-images.githubusercontent.com/97012561/171354566-9ab75ed1-cba2-4896-865f-d67f9de5171d.png">


## 배경 이미지 지정하기  
* 웹 요소에 배경 이미지를 넣는 background-images 속성  
  -`기본형 -> background-image: url('이미지 파일 경로')`  
  -파일 경로는 웹 문서를 기준으로 상대 경로를 지정할 수 있고, http://로 시작하는 절대경로를 사용할 수 있다.  

```css
<style>
  body { background-image: url('images/bg1.jpg');}
</style>
```

* 배경 이미지의 반복 방법을 지정하는 background-repeat 속성  
  -배경 이미지를 가로와 세로 중에서 어떤 방향으로 반복할지 지정하거나,   
    반복하지 않고 한 번만 나타나게 할 수 있다. 
    
|      종류 |              설명                   |
|----------|------------------------------------|
|repeat|브라우저 화면에 가득 찰 때까지 가로와 세로 바복. 기본값|
|repeat-x|브라우저 화면 너비에 가득 찰 때까지 가로 반복|
|repeat-y|브라우저 화면 너비에 가득 찰 때까지 세로 반복|
|no-repeat|한 번만 표시하고 반복 안 함|
  
 
 * 배경 이미지의 위치를 조절하는 background-position 속성  
   -속성값을 두 개로 한다면 첫 번째 값은 수평 위치의 값이 되고 두 번째 값은 수직 위치의 값.  
   -속성값을 하나로 지정하면 수평 위치값으로 간주하고,수직 위칫값은 50%나 center로 간주한다.  


* 배경 이미지의 적용 범위를 조절하는 background-origin 속성 
  -박스 모델에 패딩이나 테두리가 있다면 배경 이미지를 패딩까지 표시하거나 테두리까지 포함해서 표시할 수 있다.  
  
|      종류 |              설명                   |
|----------|------------------------------------|
|content-box|박스 모델에서 내용 부분에만 배경 이미지를 표시 기본값|
|padding-box|박스 모델에서 패딩까지 배경 이미지를 표시|
|border-box|박스 모델에서 테두리까지 배경 이미지를 표시|

* 배경 이미지를 고정하는 background-attachment 속성  
  -배경 이미지가 있는 웹 문서를 웹 브라우저에서 열고 스크롤 막대를 위아래로 조절하면  
   문서 전체가 움직이으모 배경 이미지도 함께 이동하지만  background-attachment 를 사용하면 이미지 고정 가능  
 
 |      종류 |              설명                   |
|----------|------------------------------------|
|scroll|화면을 스크롤하면 배경 이미지도 스크롤된다. 기본값|
|fixd|화면을 스크롤하면 배경 이미지는 고정되고 내용만 스크롤됨.|


* 배경 이미지 크기를 조절하는ㅌ background-size 속성  

 |      종류 |              설명                   |
|----------|------------------------------------|
|auto|원래 배경 이미지 크기만큼 적용. 기본값|
|contain|요소 안에 배경 이미지가 다 들어오도록 이미지를 확대 축소.|
|cover|배경 이미지로 요소를 모두 덮도록 이미지를 확대 축소.|
|<크기>|이미지의 높이와 너비를 지정.|
|<백분율>|백분율로 지정하여 확대 축소.|


## 그러데이션 효과로 배경 꾸미기  

#### 선형 그러데이션  
  -색상이 수직, 수평 또는 대각선 방향으로 일정하게 변하는 것을 말한다.  
  -liner-gradient로 색상이 어느 방향으로 바뀌는 지, 어떤 색상으로 바뀌는지 알려 주어야 한다.  
  -`기본형 -> liner-gradient(to <방향>,또는 <각도>, <색상 중지점>, [<색상 중지점>, ...]);`. 

##### 방향  
 -그러데이션 방향 지시시 끝 지점을 기준으로 to예약어와 함께 사용. to 다음에 방향을 나타내는 예약어를 최대 2개까지 사용.  
 -수평 방향을 나타내는 left,right, 수직 방향을 나타내는 top,bottom을 사용.  
 -ex) to right, to right top 사용.  

``` css
<style>
/*방향을 사용해 선형 그러데이션 만들기*/
.grad {
	background: blue;
  background: linear-gradient(to right bottom, blue,white);
  /* 왼쪽 위에서 오른쪽 아래 방향으로, 파랑에서 흰색으로 */
}
</style>

```
<img width="300" alt="스크린샷 2022-06-02 오후 2 39 09" src="https://user-images.githubusercontent.com/97012561/171560440-88b3ba0a-af1f-4e7d-ad15-794cf388f858.png">


##### 각도  
 -그러데이션에서 색상이 바뀌는 방향을 알려주는 방법  
 -deg로 표기  
 -각도에 따른 방향은 윗부분이 0deg이고, 시계방향으로 회전하면서 90deg,180deg 이다.  

``` css 
/*각도를 사용해 선형 그러데이션 만들기*/
<style>
.grad {
  background: #f00; /*css를 지원하지 않는 웹 브라우저용*/
  background: linear-gradient(45deg, #f00,#fff); /*45도 방향,빨간색에서 흰색으로*/
}
</style>
```
<img width="300" alt="스크린샷 2022-06-02 오후 2 46 43" src="https://user-images.githubusercontent.com/97012561/171561392-3f5a44b8-b5fe-413e-9495-b1e01b41e2e2.png">

##### 색상 중지점  
 -2가지 이상의 그러데이션을 만들려면 색상이 바뀌는 부분을 지정해야한다.  
 -싐표(,)로 구분  

```css
.grad {
  background: #06f; /*css를 지원하지 않는 웹 브라우저용*/
  background: linear-gradient(to bottom, #06f, white 30%, #06f); /*웨에서부터 30% 위치에 색상 중지점 지정*/
}
```
<img width="300" alt="스크린샷 2022-06-02 오후 2 59 16" src="https://user-images.githubusercontent.com/97012561/171562955-607f51bd-0fe1-497a-abd5-d5d58c978264.png">


#### 원형 그러데이션  
 -타원의 중심에서부터 동심원을 그리며 바깥 방향으로 색상이 바뀜.  
 -색상이 바뀌기 시작하는 원의 중심과 크기를 지정하고 그러데이션의 모양을 선택.  
 -`기본형 -> radial-gradient(<모양> <크기> at <위치>, <색상 중지점>, [<색상 중지점>, ...])`  

##### 모양  
 -원형(circle) 과 타원형(ellipse) , 모양 지정 안 하면 타원형으로 인식됨  
 
```css
/* 타원형 원형 그러데이션 */
.grad1{
   background:red;
   background:radial-gradient(white, yellow, red); 
   /* 타원형으로 흰색, 노란색, 빨간색으로 바뀌는 그러데이션 *
}
```
<img width="300" alt="스크린샷 2022-06-02 오후 3 18 43" src="https://user-images.githubusercontent.com/97012561/171565545-0e9e2316-92f4-4dec-943a-5304159fb770.png">

```css
/* 원형 그러데이션 */
.grad2{
  background:red;
  background:radial-gradient(circle, white, yellow, red);  
  /* 원형으로 흰색, 노란색, 빨간색으로 바뀌는 그러데이션 */
}
```

<img width="300" alt="스크린샷 2022-06-02 오후 3 19 59" src="https://user-images.githubusercontent.com/97012561/171565749-21542098-9f28-4418-af45-cac98789b684.png">

##### 크기 속성값
 -farthest-corner: 중심에서 가장 먼 코너에 그라데이션을 닿게 한다. 기본값  
 -farthest-side: 중심에서 가장 먼 사이드에 그라데이션을 닿게 한다.  
 -closest-corner: 중심에서 가장 가까운 코너에 그라데이션을 닿게 한다.  
 -closest-corner: 중심에서 가장 가까운 사이드에 그라데이션을 닿게 한다.  

* result
<img width="300" alt="스크린샷 2022-06-02 오후 3 32 12" src="https://user-images.githubusercontent.com/97012561/171567545-fd145ff4-7e82-4632-a256-e9d2074347ef.png">

##### 위치  
 -중심의 위치를 바꾼다. 
 -at 사용
 -`background: radial-gradient(circle at 20% 20%,white,blue); `  

* result  

<img width="300" alt="스크린샷 2022-06-02 오후 3 34 16" src="https://user-images.githubusercontent.com/97012561/171567869-c1553932-a5f5-403d-aff6-095e4411e734.png">

##### 색상 중지점  
 -`background:radial-gradient(yellow, white, orange);  
  /* 노란색에서 흰색을 거쳐 주황색으로 바뀌는 타원형 그러데이션 */`
  
<img width="300" alt="스크린샷 2022-06-02 오후 3 37 07" src="https://user-images.githubusercontent.com/97012561/171568235-a61953c8-518d-4210-a849-c181a081b168.png">


`background:radial-gradient(yellow, white 10%, orange 60%);   /* 노란색에서 10% 위치의 흰색, 60% 위치의 주황색으로 바뀌는 타원형 그러데이션 */`

<img width="300" alt="스크린샷 2022-06-02 오후 3 37 32" src="https://user-images.githubusercontent.com/97012561/171568309-8f6243d3-c679-487b-b39a-4ff5f8cab18a.png">
