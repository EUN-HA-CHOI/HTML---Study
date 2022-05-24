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
```css
기본값 -> font-style: normal | italic | oblique 
```

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
```css
 color: <색상>
``` 
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
* 예시 결과  
<img width="639" alt="스크린샷 2022-05-24 오후 4 34 25" src="https://user-images.githubusercontent.com/97012561/169975001-887fd58f-62d6-475f-88b1-dafe2ee43405.png">


