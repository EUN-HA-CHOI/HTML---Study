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

ㅊㅊ
