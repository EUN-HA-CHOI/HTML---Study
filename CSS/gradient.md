```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>css3 : gradient</title>
  <style>
    div {
      width: 200px;
      height: 200px;
    }

    .grad1 {
      background: #f00;
      background: linear-gradient(to bottom, #f00, #00f);
    }

    /*방향 top, left,bottom,right,top left,45deg 각도
      to bottom, to right, to bottom right, 45deg 각도
      사각색 , 끝색
    */

    .grad2 {
      background: #f00;
      background: linear-gradient(to bottom right, #f00, #00f);
    }

    .grad3 {
      background: #f00;
      background: linear-gradient(45deg, #f00 0%, #0f0 50%, #00f 100%);
    }

    /*방향 , 색상 위치 , 색상 위치*/

    .grad4 {
      background: linear-gradient(45deg, #f00 0%, orange 15%, yellow 30%, green 45%, #00f 60%, navy 75%, purple 100%);
    }

    .grad5 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(#f00 0%, #0f0 50%, #00f 100%);
    }

    .grad6 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(circle, #f00 0%, #0f0 50%, #00f 100%);
    }

    /*closest-side, contain 그라데이션이 가장 가까운 면과 만난다.
     closest-corner 가장 가까운 꼭지점까지 채움.
     farthest-side 가장 멀리있는 면과 만난다.
      farthest-corner ,cover  가장 멀리있는 꼭지점까지 채움 
*/

    .grad7 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(closest-side at 30% 30%, #f00 0%, #0f0 50%, #00f 100%);

    }

    .grad8 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(closest-corner at 30% 30%, #f00 0%, #0f0 50%, #00f 100%);

    }

    .grad9 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(farthest-side at 30% 30%, #f00 0%, #0f0 50%, #00f 100%);

    }

    .grad10 {
      background: #f00;
      width: 500px;
      height: 300px;
      background: radial-gradient(farthest-corner at 30% 30%, #f00 0%, #0f0 50%, #00f 100%);

    }

    .grad11 {
      background: repeating-linear-gradient(yellow 0px, yellow 20px, red 20px, red 40px);
    }

    .grad12 {
      background: repeating-radial-gradient(yellow 0px, yellow 20px, red 20px, red 40px);
    }

    .grad13 {
      width: 370px;
      height: 50px;
      background: #f8ffe8;
      background: linear-gradient(to bottom, #f8ffe8 0%, #e3f5ab 33%, #b7df2d 100%);
      border-radius: 8px;
      text-align: center;
      line-height: 50px;
      color: #fff;
      font-weight: bold;
      font-size: 20px;
      text-shadow: 0 -1px 2px #000;
    }
  </style>
</head>

<body>
  <h1>그라데이션</h1>
  <div class="grad1"></div>
  <div class="grad2"></div>
  <div class="grad3"></div>
  <div class="grad4"></div>
  <div class="grad5"></div>
  <div class="grad6"></div>
  <div class="grad7"></div>
  <div class="grad8"></div>
  <div class="grad9"></div>
  <div class="grad10"></div>
  <div class="grad11"></div>
  <div class="grad12"></div>
  <div class="grad13">button</div>
</body>

</html>
```
![image](https://user-images.githubusercontent.com/97012561/183784005-d0a19ead-5c65-4fad-8c5b-17954bc1424c.png)
![image](https://user-images.githubusercontent.com/97012561/183784050-61afdb18-8494-4891-a6ce-4d1ffc434e1a.png)
![image](https://user-images.githubusercontent.com/97012561/183784104-f1d27963-01b4-4da3-a49a-bf4cf4badb83.png)

