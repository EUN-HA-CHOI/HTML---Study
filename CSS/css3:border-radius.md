```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>css3 : border-raius</title>
  <style>
    h1 {background-color: green; width: 500px; height: 100px;
        border: 10px double yellow; text-align: center; 
        color: white; line-height: 100px; border-radius: 30px 0 ;}
        /*top-elft top-right bottom-right bottom-left*/
    li {list-style-type: none; background-color: #000; margin: 20px;
        color: #fff; width: 200px; height: 200px; text-align:center;
        line-height: 40px; font-weight: bold;}
    .c1 {background-color: #f00; border-radius: 100px;}
     /*원은 whidth,height 값의 1/2로 지정하면 된다.*/
     .c2 {background-color: blue; border-radius: 100px;}
     .c3 {height: 100px; background-color: #f00; border-radius: 100px 100px 0 0;}
     .c4 {height: 100px; background-color: blue; border-radius: 0 0 100px 100px;}
     .c5 {width:100px; height:100px; background-color: #f00; border-radius: 100px 0 0 0;}
     .c6 {width: 100px; height: 100px; background-color:  blue; border-radius: 0 0 0 100px;}     
  </style>
</head>
<body>
  <h1>css3 : border-raius</h1>
  <ul>
    <li class="c1">원 그리기</li>
    <li class="c2">원 그리기</li>
    <li class="c3">반원 그리기</li>
    <li class="c4">반원 그리기</li>
    <li class="c5">1/4원 그리기</li>
    <li class="c6">1/4원 그리기</li>
  </ul>
</body>
</html>
```

