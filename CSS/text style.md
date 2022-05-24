## 글꼴 관련 스타일  
* 글꼴을 지정하는 font-family 속성  
```css
기본형 -> font-family:<글꼴 이름> | [ <글꼴 이름> , <글꼴 이름>] 
body { font-family: "맑은 고딕", 돋움 , 굴림 }
```

* 글자 크기를 지정하는 font-size 속성  
``` css
기본형 -> font-size: <1절대 크기> | <2상대 크기> | <3크기> | <4백분율>
/*1브라우저에서 지정한 글자 크기
  2부모 요소의 글자 크기를 기준으로 상대적인 글자 크기 지정
  3브라우저와 상관없이 글자 크기 직접 지정
  4부모 요소의 글자 크기를 기준으로 백분율% 표시*/
```  

* 이탤릭체로 글자를 표시하는 font-style 속성  
`기본값 -> font-style: normal | italic | oblique `

* 글자 굵기를 지정하는 font-weight 속성  
``` css
기본값 -> font-weight: 1.normal | 2.bold | 3.bolder |4.ligter | 5.100 | 200 |....| 800 | 900
/*1기본값
  2굵게
  3원래보다 더 굵게
  4원래보다 더 가늘게
  100~900 사이의 굵기를 표현하며 100은 가장 가늘게, 900은 가장 굵게*/
```

## 웹 폰트 사용하기  
##### 웹 폰트를 사용하려면 문서 작성시 글꼴 정보를 함께 저장해야 한다.  
``` css
기본형 -> @font-face {
           font-family: <글꼴 이름>;
           src: <글꼴 파일>[<글꼴 파일>, <글꼴 파일>,.....];
         }
```

## 텍스트 관련 스타일  
* color 속성  
`color: <색상>`
 
* 웹 문서의 소스로 색상 표현 방법  
   * 16진수로 표현하는 방법  
   * hsl 과 hsla로 표현하는 방법  
   * 색상을 영문명으로 표현하는 방법  
   * rgb 와 rgba로 표현하는 방법  

* 텍스트를 정렬하는 text-align 속성  
``` css  
기본형 -> text-align: start | and | left | right | center | justify | match-parent

left: 왼쪽 정렬
right: 오른쪽 정렬
center: 중앙 정렬
justify: 양쪽 정렬 (자동 줄바꿈시 오른쪽 경계선 부분 정리)

**예시
.center {
        text-align: center;
      }
      .justify {
        text-align: justify;
      }
```  
##### text-align 예시 
<img width="639" alt="스크린샷 2022-05-24 오후 4 34 25" src="https://user-images.githubusercontent.com/97012561/169975001-887fd58f-62d6-475f-88b1-dafe2ee43405.png">  

* 줄 간격을 조절하는 line-height 속성  
``` css
/*예시*/
<style>
.small-line {
        line-height:0.7;     /*글자 크기의 0.7배 줄 간격*/
      }
.big-line {
        line-height:2.5;      /*글자 크기의 2.5배 줄 간격*/
      }
</style>
<body>                                        
   <p>껍질에 붉은 빛이 돌아 ~통통하다.</p>           
   <p class="small-line">껍질에 붉은 빛이 돌아 ~ 통통하다.</p>
   <p class="big-line">껍질에 붉은 빛이 돌아 통통하다.</p>
</body>
```
##### line-height 예시 
<img width="631" alt="스크린샷 2022-05-25 오전 12 30 20" src="https://user-images.githubusercontent.com/97012561/170074370-3379d6e8-b95f-4f93-84ed-2b7a97134a43.png">


* 텍스트의 줄을 표시하거나 없애 주는 text-decoration 속성  
``` css
/*예시*/
<body>
    <h1>text-decoration 속성</h1>
    <p style="text-decoration:none">none</p>
    <p style="text-decoration:underline">underline</p>
    <p style="text-decoration:overline">overline</p>
    <p style="text-decoration:line-through">line through</p>
  </body>
```

##### text-decoration 예시  
<img width="293" alt="스크린샷 2022-05-25 오전 12 42 12" src="https://user-images.githubusercontent.com/97012561/170076817-5ad65c0a-a3ec-42e1-9d5a-a70d191a5958.png">  

* 텍스트에 그림자 효과를 추가하는 text-shadow 속성  
`기본형 -> text-shadow: none | <가로 거리> <세로 거리> <번짐 정도> <색상> `
```css
/*텍스트에 그림자 효과 추가하기*/
<head>
  <meta charset="UTF-8">
  <title>text-shadow</title>
  <style>    
    h1 { 
      font-size:60px;
    } 
    .shadow1 {
      color:red;
      text-shadow:1px 1px black;
    }
    .shadow2 {
      text-shadow:5px 5px 3px #ffa500;
    }
    .shadow3 {
      color:#fff;
      text-shadow:7px -7px 20px #000;
    }
  </style>
</head>
<body>
  <h1 class="shadow1">HTML</h1> 
  <h1 class="shadow2">CSS</h1>
  <h1 class="shadow3">자바스크립트</h1>
</body>
```
##### text-shadow 
<img width="327" alt="스크린샷 2022-05-25 오전 12 45 56" src="https://user-images.githubusercontent.com/97012561/170077600-6b8f8eda-1c40-4826-9d4d-460e058730e2.png">  

* 텍스트의 대소 문자를 변환하는 text-transform 속성  
 
|    종류   |         설명           |
|----------|-----------------------|
|capitalize| 첫 번째 글자를 대문자로 변환 |
|uppercase| 모든 글자를 대문자로 변환     |
|lowercase| 모든 글자를 소문자로 변환     |  

```css
 <style>    
    .trans1 {
      text-transform: capitalize;
    }
    .trans2 {
      text-transform: uppercase;
    }
    .trans3 {
      text-transform: lowercase;
    }
  </style>
</head>
<body>
  <p class="trans1">html</p> 
  <p class="trans2">css</p>
  <p class="trans3">javascript</p>
</body>
```
##### text-transform 예시  
<img width="78" alt="스크린샷 2022-05-25 오전 1 01 12" src="https://user-images.githubusercontent.com/97012561/170080839-d0cf1b5b-af64-4327-8df3-cd6dc0a7dc90.png">


* 글자 간격을 조절하는 letter-spacing , word-spacing 속성  
``` css
<style>  
      p {
        font-family:Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
        font-size:30px;
        text-shadow:3px 3px 1px #ccc;  /* 오른쪽 아래로 파란색 그림자 */
      }
      .spacing1 {
        letter-spacing:0.2em;  /* 글자 간격 0.2em */
      }
      .spacing2 {
        letter-spacing:0.5em;  /* 글자 간격 0.5em */
      }      
    </style>
  </head>
  <body>
    <p>CSS</p> 
    <p class="spacing1">CSS</p>
    <p class="spacing2">CSS</p>
  </body>
``` 
#####  letter-spacing 
<img width="90" alt="스크린샷 2022-05-25 오전 1 04 39" src="https://user-images.githubusercontent.com/97012561/170081478-db8633e2-6f64-4154-a2c7-a4d79c853f28.png">



