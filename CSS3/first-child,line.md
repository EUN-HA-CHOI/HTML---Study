### first-child 가상 클래스, 형제선택자, + 인접형제선택자  

* first-child (html)
```html
<body>
  <div class="child">
    <p>
      first-child 가상 클래스는 첫 번째 자식 요소에만 스타일을 적용할 수 있는 선택자입니다.
    </p>
    <p>child 클래스의 두 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
    <p>child 클래스의 세 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
  </div>
  <h2>first-child 가상 클래스</h2>
  <div class="child">
    <p>
      first-child 가상 클래스는 첫 번째 자식 요소에만 스타일을 적용할 수 있는 선택자입니다.
    </p>
    <p>child 클래스의 두 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
    <p>child 클래스의 세 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
  </div>
  <div class="child">
    <p>
      first-child 가상 클래스는 첫 번째 자식 요소에만 스타일을 적용할 수 있는 선택자입니다.
    </p>
    <p>child 클래스의 두 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
    <p>child 클래스의 세 번째 자식 요소에는 스타일이 적용되지 않습니다.</p>
  </div>
  
</body>
```

* first-child (css)
```css
 <style>
    div > p:first-child {color: green}
    div > p:last-child {color: blue;}

    h2 + div {font-weight: bold; font-style: italic;}
    /*h2에 인접한 형제인 div만 선택*/

    h2 ~ div {text-decoration: underline;}
    /*h2 뒤에 있는 형제인 div는 모두 선택*/
  </style>
```
![image](https://user-images.githubusercontent.com/97012561/185343531-08037fa8-a714-4db9-af3a-43c1b530837b.png)

***

### first-line , first-letter  

* first-line , first-letter (html)
```html
<body>
  <div class="line">
    <p>
      요소의 첫번째 줄에 있는 콘텐츠만 선택하여 스타일을 지정할 때 사용하는 선택자 방식으로 first-line 가상 요소 선택자라고 부른다.
      first-line 가상 요소 선택자를 지정할 경우 고정된 영역이 아닌 웹브라우저 크기에 따라 유동적으로 스타일이 적용됩니다.
    </p>
  </div>
  <div class="letter">
    <p>
      요소의 첫번째 글자만 선택하여 스타일을 지정할 때 사용하는 선택자방식
    </p>
  </div>  
```

* first-line , first-letter (css)
```css
<style>
    .line > p:first-line {text-decoration: underline;}
    .letter > p:first-letter {font-size: 5em;}
  </style>
```

![image](https://user-images.githubusercontent.com/97012561/185344045-0fadfbf6-b604-44b6-a53b-cdae00f578b0.png)
