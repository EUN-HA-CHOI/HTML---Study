
* font 정리
 
```css
<style>
.size{font-size: 30px;}

.basic{font-size: 16px;} /* body 기본글씨크기 : 16px , 100% , 1em */

.family{font-family: Dotum, "돋움", sans-serif;}
/* 기본글꼴: 굴림, serif 명조, sans-serif 고딕 */

.weight{font-weight: bold;}

strong,h3{font-weight: normal;} /* 그룹선택자 */

.style{font-style: italic;}

em,address{font-style: normal;}

.variant{font-variant: small-caps;  } /* 작은 대문자로 바꿔줌 */

.line{line-height: 300%;} 

.font{font: bold italic small-caps 20px /1.5 Dotun, "돋움", sans-serif;}

/* font 순서 중요 : 
 font-style  font-weight font-size line-height font-family */

.font2{font:20px Dotum, "돋움", sans-serif;}

.indent{text-indent: 50px;} /* 문단의 첫줄만 들여쓰기, -50px 내어쓰기 */

.underline{text-decoration: underline;} /* underline 및줄, overline 윗줄, line-through 취소선 */

a{text-decoration: none; color: black;}

.align{text-align: center;} /* 가로 정렬: left right center jutify 양쪽정렬 */

.letter{letter-spacing: 30px;}

.word{word-spacing: 30px;}

.top{vertical-align: top;}

.middle{vertical-align: middle;}

.bottom{vertical-align: bottom;}

.upper{text-transform: uppercase;} /* 영어 대문자 */

.lower{text-transform: lowercase;} /* 영어 소문자 */

.capital{text-transform: capitalize;} /* 영어 첫글자 대문자로 */

.pre{white-space: pre;}
</style>
```

```html
<body>
  <p class="size">글자크기30</p>
  <p class="basic">글자크기16</p>
  <p class="family">글꼴돋움</p>
  <p>글꼴</p>
  <p class="weight">글자굵게</p>
  <p><strong>강한강조</strong></p>
  <h3>제목</h3>
  <p class="style">글자기울임</p>
  <p><em>약한강조</em></p>
  <address>Copyright</address>
  <p class="variant">Home,home</p>
  <p class="line">줄간격,행간 300%</p>
  <p>기본</p>
  <p class="font">FONT ,font 라는 속성에 다 값을 넣어서 사용가능한다, 이때 순서가 중요</p>
  <p class="font2">font 속성에서는 반드시 font-size 와 font-family가 들어가야한다.</p>
  <p class="indent">들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50 들여쓰기 50들여쓰기 50
    들여쓰기 50들여쓰기 50들여쓰기 50들여쓰기 50들여쓰기 50들여쓰기 50들여쓰기 50들여쓰기 50
  </p>
  <p class="underline">글자밑줄</p>
  <p><a href="#">네이버 바로가기</a></p>
  <p class="align">가로정렬 왼쪽,가운데,오른쪽,양쪽가로정렬 가로정렬 왼쪽,가운데,오른쪽,양쪽가로정렬 가로정렬 왼쪽,가운데,오른쪽,양쪽가로정렬 가로정렬 왼쪽,가운데,오른쪽,양쪽가로정렬</p>
  <p class="letter">자간 -3,글자와 글자사이 간격</p>
  <p class="word">단어와 단어 사이 간격</p>
  <p><img src="naver.gif" alt="네이버" class="">세로정렬</p>
  <p><img src="naver.gif" alt="네이버" class="top">세로정렬 위</p>
  <p><img src="naver.gif" alt="네이버" class="middle">세로정렬 가운데</p>
  <p><img src="naver.gif" alt="네이버" class="bottom">세로정렬 아래</p>
  <p class="upper">text-transform 영문 소문자를 대문자로</p>
  <p class="lower">text-transform 대문자를 소문자로</p>
  <p class="capital">text-transform 첫글자만 대문자로</p>
  <p class="pre">공백문자를 
    위해서 
    whith-space를 
    사용</p>
  <p class="nowrap">공백처리 공백처리 공백처리 공백처리 공백처리 공백처리</p>
```
