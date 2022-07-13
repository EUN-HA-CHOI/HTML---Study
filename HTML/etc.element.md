## 기타 Element

```html
<body>
  <!-- ins 추가글 , del 삭제글 -->
  <p>
    <ins>할인가:1.000원</ins>
    <del>판매원가:5,000원</del>
  </p>

  <!-- sup 윗첨자, sub 아래첨자 -->
  <p>X<sup>2</sup> , H<sup>2</sup>0</p>

  <!-- 특수기호 & , < , > , " , ', © -->
  <p>&amp; , &lt;, &gt;, &quot;, &#39;, &copy;, &middot; </p>

  <!-- pre : 텍스트에만 적용됨 -->
  <pre>봄
     
    여름 가을 
    
    겨울
  </pre>

  <!-- code : html에 css삽입할 때 코드로 인식해라 -->
  <p><code>td{width:100px;height:100px;}</code></p>

  <!-- time요소, datetime속성= "년월일T시분초,밀리초(1000분의1초)
    z국제표준시, + - 지역표준시" -->
  <time datetime="2022-07-12T10:45:59.000Z">2022-07-12</time>

  <!-- mark 요소, 키워드 강조 -->
  <p><mark>html5</mark>와 css3는 w3c 국제 표준화 단체에서 권고안을 작성해서 배포합니다
    <mark>html5</mark>를 사용하면 반응협웹 뿐만아니라 <mark>html5</mark>웹앱을 만들수 있습니다.
    또한 하이브리드앱도 html5로 만들 수 있습니다.
  </p>

  <!-- i요소: 기울임, b요서: 굵게, small요소:작은글씨 -->
  <p><i>기울임, 외국어, 분류학적인용어, 기술용어, 대본 지문, 생각이나
      손으로 직접쓴 글등 다른 텍스트와 구별하기 위해</i></p>

  <p><b>중요하지는 않지만 굵게 보이게 하기 위해서 쓴다,</b></p>

  <p><small>작은 글씨, 푸터 안에 정보, 이용약관, 단서와 세부사항과 같은 부가적인 주석,
      짧은 문장에 사용</small></p>
  
  <!-- progress: 다운로드 진행표시줄로 사용,
       meter요소:디스크 사용량등 범위가 지정된 요소를 표시할 때 사용 -->
  
  <p>다운로드 상태:
    <progress max="100" value="52"><span>0</span>%</progress>
  </p>

  <p>현재 디스크 총 사용량:
     <meter min="0" max="320" value="20" low="50" high="250"
     optimum="320">64GB</meter>
  </p>

  <!-- figure, figcaption:차트,그래프,이미지,소스코드,다이어그램을 
    표시하는 figure 
    설명 figcaption-->
  <figure>
    <img src="cat.png" alt="고양이 사진" />
    <figcaption>고양이 사진</figcaption>
  </figure>

  <figure>
    <img src="computer-mouse-pic.png" alt="컴퓨터 마우스" />
    <img src="computer-mouse-pic.png" alt="컴퓨터 마우스" />
    <img src="computer-mouse-pic.png" alt="컴퓨터 마우스" />
    <figcaption>컴퓨터 마우스 사진</figcaption>
  </figure>
</body>
```



<img width="481" alt="스크린샷 2022-07-13 오후 11 17 29" src="https://user-images.githubusercontent.com/97012561/178755791-213ab2a4-9c33-49dd-9422-0218521aa7c6.png">
<img width="487" alt="스크린샷 2022-07-13 오후 11 17 46" src="https://user-images.githubusercontent.com/97012561/178755857-4787717f-16ae-4e4f-bd10-a06c526e836e.png">
