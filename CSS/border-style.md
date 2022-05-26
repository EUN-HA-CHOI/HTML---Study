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

