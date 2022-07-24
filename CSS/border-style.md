## 테두리 스타일 지정하기  
* 박스 모델의 방향 살펴보기  
  -박스 모델은 상하좌우 4개의 방향이 있어서 테두리나 마진,패딩 등을 지정할 때 한꺼번에 똑같이 지정하거나, 다르게 지정 가능.  
  -박스 모델의 방향으로 맨 윗부분은 top , 오른쪽은 right , 아랫부분은 bottom, 왼쪽은 left 라고 한다.  
  -맨 위부터 시작해서 top -> right -> bottom -> left처럼 시계방향 순서이다. *중요!  

* 테두리 스타일을 지정하는 border-style 속성  
  -solid : 테두리를 실선으로 표시  
  -dotted : 테두리를 점선으로 표시  
  -dashed : 테두리를 짧은 직선으로 표시  
  -double : 테두리를 이중선으로 표시  

``` css  
 #box1 { border-style:solid } /*실선*/
 #box2 { border-style:dotted } /*점선*/
 #box3 { border-style:dashed } /*짧은 점선*/
```
<img width="400" alt="스크린샷 2022-05-26 오후 3 25 45" src="https://user-images.githubusercontent.com/97012561/170430063-cd9f3726-8949-4e07-b96d-4cd68f4ffc3b.png">


* 테두리 두께를 지정하는 border-width 속성  
`border-width: <크기> | thin | medium | thick`

```
 #box1 {
      border-width:2px;  /* 네 방향 모두 2px */ 
    }
    #box2 {
      border-width:thick thin;  /* top & bottom - thick, left & right - thin */
    }
    #box3 {
      border-width:thick thin thin;  /* top - thick, right - thin, bottom - thin, left - thin */ 
    }
    #box4 {
      border-width:10px 5px 5px 10px;  /* top - 10px, right - 5px, bottom - 5px, left - 10px */
    }
```
<img width="400" alt="스크린샷 2022-05-26 오후 3 37 16" src="https://user-images.githubusercontent.com/97012561/170431906-9216aea9-4e99-4fd4-93bf-0801ae5491e9.png">


* 테두리 색상을 지정하는 border-color 속성  
```css
#box1 { border-color:red;	}  /* 전체 테두리 - 빨강 */
#box2 { 
  border-top-color:blue; /* 위쪽 테두리 - 파랑 */
  border-left-color:red;  /* 왼쪽 테두리 - 빨강 */
} 
```
<img width="400" alt="스크린샷 2022-05-26 오후 4 17 21" src="https://user-images.githubusercontent.com/97012561/170438000-aaa4f87c-1397-4e4f-b875-b7f312fef904.png">

* 테두리 스타일 묶어 지정하는 border 속성  
  -테두리 스타일과 두께, 색상을 한꺼번에 표현  
 
```css
<style>
	h1 {
		padding-bottom: 5px;
		border-bottom: 3px solid rgb(75, 70, 70); /* 아래쪽 테두리만 3px짜리 회색 실선*/
	}
	p {
		padding: 10px;
		border: 3px dotted blue; /* 모든 테두리를 3px짜리 파란 점선 */
	}
</style>
```

<img width="493" alt="스크린샷 2022-05-26 오후 4 39 12" src="https://user-images.githubusercontent.com/97012561/170441541-8487eaf7-bcfa-4844-99a1-7a32096a8985.png">

* 둥근 테두리를 만드는 border-radius 속성  
`border-radius: <크기> | <백분율>`  

`border-radius: 25px;  /* 모든 꼭짓점을 둥글게 */`

<img width="400" alt="스크린샷 2022-05-26 오후 5 03 58" src="https://user-images.githubusercontent.com/97012561/170445574-d2adb4e8-1177-4a66-bdd4-ebc743d21814.png">

<hr/>

* 박스모델 실제 너비감 결정하기 ! (헷갈림주의)

```
.container {
  background-color: orange;
  width: 400px;
  border: 1px solid red;
}

.box {/Users/choieunha/Desktop/07.18/border.html
/Users/choieunha/Desktop/07.18/box2.html
  color: white;
  background-color: green;
  width: 200px;
  height: 30px;
  padding: 20px;
  border: 5px dashed black;
  margin: 15px;
}
```
  예를 들어 전체 너비(width)를 400px로 설정했다. 그 안에 박스모델의 너비는 200px 이라고 가정하자 실제 화면에서 차지하는 너비는 padding과 border의 두께까지 고려해야 한다. 위의 예제의 box 실제 너비는 좌우 padding 값과 좌우 border 값을 더한 250px이 됩니다.
  
  위의 예제의 경우 box 실제 너비는 : 200px + (20px * 2) + (5px * 2) = 250px 이다.
  container의 실제 너비는 : 400px + (0px * 2) + (1px * 2) = 402px 이다.
  
  만약 box를 container 속에 딱 맞게 하려면 width 값은 얼마일까? 먼저 box의 margin 속성값을 0으로 설정하여 container와의 간격을 제거해야한다. 다음 container의 좌우 padding 값과 좌우 border 값을 빼줘야 된다. 
400px - (20px * 2) - (5px * 2) = 350px
### (예제)박스 모델 3단 만들기

```html
<body>
  <div id="wrap">
    <div id="top">top</div>
    <div id="middle">middle</div>
    <div id="bottom">bottom</div>
  </div>  
</body>
```

```css
<!-- 
전체 wrap 실제크기 가로 600px, 세로 600px 
박스 3개크기 동일 - 가로 600px, 세로 200px
안쪽 여백 동일 - 20px
테두리선 동일 - 5px
바깥쪽여백 동일 - 11px
전체 wrap 여백 - 10px
-->

<style>
  * {
    padding: 0;
    margin: 0;
  }
  body {
    font-size: 30px;
    color: #fff;
    font-weight: bold;
  }
  #wrap {
    width: 580px;
    height: 580px;
    background-color: yellow;
    padding: 10px;
  }
  #top {
    width: 530px;
    height: 136px;
    background-color: red;
    border: 5px solid black;
    padding: 20px;
    margin-bottom: 11px;
  }
  #middle {
    width: 530px;
    height: 136px;
    background-color: green;
    border: 5px solid black;
    padding: 20px;
    margin-bottom: 11px;
  }
  #bottom {
    width: 530px;
    height: 136px;
    background-color: blue;
    border: 5px solid black;
    padding: 20px;
    margin-bottom: 11px;
   }
</style>
```

<img width="300" alt="스크린샷 2022-07-24 오후 8 17 24" src="https://user-images.githubusercontent.com/97012561/180644540-07ba6eb9-6ccd-4d79-bed0-e1a88d06c826.png">
