## 웹 요소의 위치 지정하기  
* 웹 요소의 위치를 정하는 left,right,top,bottom 속성  
  -position 속성으로 기준 위치를 정한 뒤 요소의 위치를 위의 속성에서 선택하고 속성값을 지정하면 된다.  

* 배치 방법을 지정하는 position 속성  

| 종류 |                    설명                           | 
|-------|------------------------------------------------|  
|static|문서의 흐름에 맞춰 배치. 기본값|
|relative|위칫값을 지정할 수 있다는 점을 제외하면 static과 같다|
|absolute|relative값을 사용한 상위 요소를 기준으로 위치를 지정해 배치|
|fixed|브라우저 창을 기준으로 위치를 지정해 배치|  

##### -absolute값을 사용할 땐 요소에 position:absolute 라고 한 후 위칫값을 지정하면 요소 중에서 position:relative를 사용한 요소를 기준으로 위치를 결정한다. 

##### -어떤 요소에 position:absolute 를 사용하려면 부모 요소에는 position:relative라고 지정해야 원하는 대로 배치할 수 있다.  

* 배경 위에 글자 표시하기  
``` css
#contents {
 background:url("../images/bg.jpg") no-repeat;
 background-size:cover;
 width:800px;
 height:500px;
 margin:0 auto;
 position:relative;
}
h1 { 
  color:#fff; 
  font-size:120px;
  text-shadow: 2px 3px 0 #000;      
  position:absolute;
  right:100px;
  bottom:100px;
}
```
 ##### 부모요소에 position:relative; 속성 추가 안 했을 때와 했을 때
<img width="350" alt="스크린샷 2022-06-01 오후 4 23 06" src="https://user-images.githubusercontent.com/97012561/171350055-bfb5f500-7d7f-4e32-b464-5899ae14b3ac.png">

<img width="350" alt="스크린샷 2022-06-01 오후 4 26 32" src="https://user-images.githubusercontent.com/97012561/171350628-b93de13c-dc74-47f5-98b3-140adc37dc98.png">


