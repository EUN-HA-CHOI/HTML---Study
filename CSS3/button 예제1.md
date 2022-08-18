* 마우스 hover 하면 색 바뀌는 버튼 예제 만들기  

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>버튼 예제1</title>
  <style>
    ul {
      list-style: none;     
    }
    li {
      display: inline-block;
    }

    li a {
      padding: 15px 15px;
      background: #ffa84c;
      background: linear-gradient(to bottom,  #ffa84c 0%,#ffa84c 19%,#ff7b0d 100%);
      color: #fff ;
      text-decoration: none;
      border-radius: 5px;
      border: 1px solid #da7c0c;
      text-shadow: 0 1px 1px rgba(0,0,0,0.3);
      box-shadow: 0 1px 2px rgba(0,0,0,0.2);
      font-size: 14px;
      line-height: 100%;
      text-align: center;
      font-family: Arial, Helvetica, sans-serif;
    }
    li a:hover {
      background: #ffa84c;
      background: linear-gradient(to bottom,  #db7c16 5%,#c98b49 49%,#d8680d 100%);
    }

    li a:active {
      position: relative;
      top:2px;
      color: rgb(223, 223, 223);
      background: #f06015;
      background: linear-gradient(to bottom,  #e07b0f 0%,#e6a259 49%,#f8b178 100%);
    }


  </style>
</head>
<body>
  <ul>
    <li><a href="#">HOME</a></li>
    <li><a href="#">HTML5</a></li>
    <li><a href="#">CSS3</a></li>
    <li><a href="#">BOARD</a></li>
    <li><a href="#">PROFILE</a></li>
  </ul>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/97012561/185345006-c50eb797-8c9d-487b-b26d-096a6cbdd671.png)
