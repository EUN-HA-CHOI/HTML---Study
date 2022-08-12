### css3 : text-shadow.   

```css
<style>
    p {
      font-family: "맑은고딕",sans-serif; font-size: 100px; font-weight: bold;
    }
    .text1 {
      color: #f00; text-shadow: 5px 5px 5px #000;
    }
    /*text-shadow: 가로 오프셋 offset, 세로 오프셋,blur radius, 그림자 색상*/
    .text2 {
      color: #00f; text-shadow: -5px -5px 5px #000;
    }
  </style>
```

```css
<style>
    p {
      font-family: "맑은고딕", sans-serif;
      font-size: 100px;
      font-weight: bold;
    }

    .text1 {
      color: #000;
      text-shadow: 0 0 4px #ccc, 0 -5px 4px #ff3,2px -10px 5px #fd3, -2px -15px 11px #f00,
         2px -19px 18px #f20;
    }
    .text2 {
      color: #000;
      text-shadow: ;
    }

  </style>
  
