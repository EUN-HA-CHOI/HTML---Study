### overflow 속성의 적용  

```html
<body>
  <h1>overflow 속성의 적용 결과</h1>
  <p class="hidden">콘텐츠의 내용이 박스의 크기를 넘어가는 경우 박스의 크기 만큼만 보이고 나머지 콘텐츠는
    보이지 않도록 숨길 수 있다.
  </p>
  <p class="scoll">박스의 크기와 콘텐츠의 내용과 상관없이 박스에 스크롤바를 생성할때는
    overflow:scroll;을 선언하면 된다. 이때 만약 박스의 크기가 콘텐츠보다 클 경우 스크롤바는 비활성화되어 나타난다</p>

  <p class="auto">콘텐츠의 내용이 박스의 크기보다 많아서 박스에 자동으로 스크롤바가 생성되도록 할 경우에 선언</p>
  <p class="visible">콘텐츠의 내용이 바스의 크기를 넘어가는 경우 박스의 크기를 무시하고 콘텐츠의 내용을 모두 보여지도록 할 때 선언,블록요소의 기본값이기도하다</p>
</body>
```

```css
<style type="text/css">
  p{width: 150px; height: 70px; border: 1px solid black; padding: 5px;}
  .hidden{overflow: hidden;}
  .scrool{overflow: scroll;}
  .auto{overflow: auto;}
  .visible{overflow: visible;}  /*기본값*/
</style>
```


<img width="150" alt="스크린샷 2022-07-22 오전 12 13 11" src="https://user-images.githubusercontent.com/97012561/180249526-97e037f6-9846-47ee-a287-4c6c6c9010de.png">

