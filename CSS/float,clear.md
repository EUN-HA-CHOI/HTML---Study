## float 속성  

<p>이미지와 글자의 위치는 어떻게 배치시키는지 결정하는 속성, 주로 레이아웃 설정에 적용됨 </p>   

* 속성     
  **inherit**: 부모 요소에서 상속  
  **left**: 왼쪽에 부유하는 블록 박스를 생성. 페이지 내용은 박스 오른쪽에 위치하며 위에서 아래로 흐름.  
  **right**: 오른쪽에 부유하는 블록 박스를 생성. 페이지 내용은 박스 왼쪽에 위치하며 위에서 아래로 흐름. 이후 요소에 clear 속성이 있으면 페이지 흐름이    달라짐. none 이 아니라면 display 속성은 무시된다.  
    none - 요소를 부유시키지 않음  

```html
<body>
  <div id="red">red</div>
  <div id="green">green</div>
  <div id="blue">blue</div>  
</body>
```

```css
<style>
  div {
    width: 200px;
    height: 200px;
    color: #000;
    font-size: 30px;
    font-weight: bold;
    display: inline-block;
  }
  #red {
    float: left;
    background-color: red;
  }
  #green {
    float: left;
    background-color: green;
  }
  #blue {
    float:left;
    background-color: blue;
  }
  /* float : left , right */
  
</style>

```
<img width="300" alt="스크린샷 2022-07-25 오후 11 57 32" src="https://user-images.githubusercontent.com/97012561/180807783-60281b66-966f-4d2d-9054-7650eeb13c9b.png">

<hr/>

## clear 속성  

- clear 속성은 float 속성이 적용된 이후 나타나는 요소들의 동작을 조절해 줍니다.
- float 값에 따라 clear 값 설정해야 float 요소의 다음 요소 제어 가능   
- float 속성값에 영향 받음  

* 속성  
  clear : none;  
  clear : left;  
  clear : right;   
  clear : both;  
  clear : initial;  
  clear : inherit;  
  
  
1. clear : left;  (왼쪽으로 float된 요소 밑으로 요소가 밀려짐)

```css
<style>
    .float {
		float: left;
    }

    .clear {
		clear: left;
    }
    </style>
```
<img width="500" alt="스크린샷 2022-07-26 오전 12 17 50" src="https://user-images.githubusercontent.com/97012561/180814232-38bebf58-0f70-43a5-85e7-60d9c6773200.png">



2. clear : right; (오른쪽으로 float된 요소 밑으로 요소가 밀려짐)

```css
<style>
    .float {
		float: right;
    }

    .clear {
		clear: right;
    }
    </style>
```

- float가 right로 지정되었기 때문에 clear도 right로 지정했다.  
  만약 float가 left인 상태이고, clear를 right로 지정되면, 화면에서는 float의 다음 요소를 제어하지 못 한다.  
  그렇기 때문에 clear:both를 사용할게 아니라면, clear는 float의 속성값에 영향을 받는다.  
 
 <img width="500" alt="스크린샷 2022-07-26 오전 12 18 20" src="https://user-images.githubusercontent.com/97012561/180814843-92cf525c-165d-40d5-9d16-30a8193d0b81.png">



3. clear : both;   
   (왼쪽 또는 오른쪽으로 float 요소 밑으로 밀려짐 /왼쪽과 오른쪽 모두 float 요소가 있다면 height가 더 높은 요소 밑으로 밀림)

```css
<style>
    .float-left {
		float: left;
    }
      
    .float-right {
		float: right;
    }

    .clear {
		clear: both;
    }
    </style>
```

<img width="500" alt="스크린샷 2022-07-26 오전 12 19 15" src="https://user-images.githubusercontent.com/97012561/180814552-6aa078cb-a92a-4400-b350-b1698cbf560c.png">

