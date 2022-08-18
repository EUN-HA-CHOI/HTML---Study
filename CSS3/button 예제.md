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

***

* 버튼 예제2

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>버튼예제</title>
  <style>
    /*화살표는 padding 으로, 글자 그림자 ,hover하면 색깔바뀜 , 누르면 살짝 내려감(posistion)가상클래스 */
    ul {
      list-style: none;

    }
    li {
      margin: 10px 0;
    }
    li a {
      display: inline-block;
      text-decoration: none; 
      font-weight: bold;
      color: white;
      border-radius: 5px;
      padding: 10px 10px;
      border: none;
    }

    .blue {
      background-color: rgb(80, 123, 172);  
      text-shadow: 1px -1px 0 #000;
      box-shadow: 0 1px 2px #000;
    }

    .blue:hover {
      background-color: rgb(225, 225, 247);
    }

    .red {
      background-color: red;
      text-shadow: 1px -1px 0 #000;
      box-shadow: 0 1px 2px #000;
    }

    .red:hover {
      background-color: rgb(236, 122, 122);
    }

    .yellow {     
      background-color: rgb(247, 177, 48);
      text-shadow: 1px -1px 0 #000;
      box-shadow: 0 1px 2px #000;
    }

    .yellow:hover {
      background-color: rgb(241, 221, 166);
    }

    li a:active {
      position: relative;
      top: 2px;
    }  /*누르면 내려옴*/
  </style>
</head>

<body>
  <ul>
    <li><a href="#" class="blue">Blue Button &raquo;</a></li>
    <li><a href="#" class="red">Red Button &raquo;</a></li>
    <li><a href="#" class="yellow">yellow Button &raquo;</a></li>
  </ul>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/97012561/185345968-f3d11051-fccc-4952-8b15-08a8ae6f268e.png)

***

*  예제3  
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>메뉴예제2</title>
  <style>
    
    ul {
      list-style: none;  
    }
    li {
      display: inline-block;
      float: left;
    }

    li a {
      padding: 15px 15px;
      background: #7d7e7d;
      background: linear-gradient(to bottom,  #7d7e7d 0%,#7d7e7d 47%,#0e0e0e 100%);
      color: #000 ;
      text-decoration: none; 
      text-shadow: 0 1px 1px rgb(250, 249, 249);
      font-size: 14px;
      text-align: center;   
      font-family: Arial, Helvetica, sans-serif;
    }
    li a:hover {
      color: #fff;
      background: #fbfffb;
      background: linear-gradient(to bottom,  #7d7e7d 0%,#7d7e7d 47%,#0e0e0e 100%);
    }

    li a:active {
      position: relative;
      top:2px;
      color: #fff;
      background: #7d7e7d;
      background: linear-gradient(to bottom,  #7d7e7d 0%,#7d7e7d 47%,#0e0e0e 100%);
    }

    ul > li:first-child a {border-radius: 5px 0 0 5px;}
    ul > li:last-child a {border-radius: 0 5px 5px 0;}
  </style>
 

</head>
<body>
  <ul>
    <li><a href="#">HOME</a></li>
    <li><a href="#">HTML5</a></li>
    <li><a href="#">CSS3</a></li>
    <li><a href="#">JQuery</a></li>
    <li><a href="#">Mobile</a></li>
    <li><a href="#">Propile</a></li>
  </ul> 
</body>
</html>
```
![image](https://user-images.githubusercontent.com/97012561/185346289-442800a4-a86d-4cf7-a1bf-5b09f9cae6fd.png)
