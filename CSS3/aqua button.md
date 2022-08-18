### 아쿠아 버튼  

```html
<body>
  <div class="button">
    <div class="aqua"></div>
    HTML5
  </div>
</body>
```

```css
<style>
    .button {
      position: relative;
      width: 120px;
      height: 24px;
      padding: 5px 5px 3px;
      border-radius: 16px;
      background: rgba(60, 132, 198, 0.8);
      background: linear-gradient(to bottom, rgba(28, 91, 155, 0.8)0%, rgba(108, 191, 255, 0.9) 90%);
      text-align: center;
      font-family: "Myriad Pro", sans-serif;
      color: #fff;
      font-weight: 800;
      box-shadow: 0 10px 16px rgba(66, 140, 240, 0.5);
      text-shadow: 1px 2px 2px rgba(10, 10, 10, 0.5);
      border-width: 2px;
      border-style: solid;
      border-color: #8ba2c1 #5890bf #4f93ca #768fa5;
    }
    /*border: 2px soild #fff
      border-top-color: ;
      border-right-color: ;
      border-bottom-color: ;
      border-left-color: ;
    */

    .aqua {
      position:absolute;
      left: 5px;
      top: 0;
      width: 123px;
      height: 1px;
      padding: 8px 0;
      background: rgba(255, 255, 255, 0.25);
      border-radius: 8px;
      background: linear-gradient(to bottom,rgba(255, 255, 255, 0.7)0%,
      rgba(255, 255, 255, 0) 95%);
    }

    .button:hover {
      top:1px;
      text-shadow: 0 0 5px rgb(255, 255, 255);     
    }
  </style>
```

![image](https://user-images.githubusercontent.com/97012561/185344665-ca676beb-1fb1-4bab-8b69-68c2c5cd75a0.png)
