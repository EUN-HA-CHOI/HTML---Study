### css3 : target  

```css
<style>
  /*선생님 코딩*/
  ul {
    list-style: none;
  }
  li {
    float: left;
    margin-right: 30px;
  }
  li a {
    color: red;
    text-decoration: none;
    font-size: 20px;
    font-weight: bold;
    padding: 5px;
    transition: all 1s ease 0s;
  }
  li a:hover {
    background: #207;
    color: #fff;
  }
  /*target 부분
  앵커링크를 클릭해서 target으로 연결되는 element 요소에 css 표시를 할 수 있다.
  */
  p:target{
    border: 2px solid #900;
    border-radius: 5px;
    background: #ffc;
    padding: 5px 8px;
  }
  /* 내가 코딩한 것
  ul > li > a{
    text-decoration: none;
    color: red;
    float: left;
    padding: 0 20px;
    transition: all 1s ease 0s;
  }
  ul>li> a:hover {
    background-color: rgb(22, 22, 44);
    color: white;
    }  */
</style>
```

[target 적용 예시](http://127.0.0.1:5500/target.html)
