## 웹 문서에 다양한 내용 입력하기  
### 텍스트 입력하기 
``` html
제목을 나타내는 <hn>
텍스트 단락을 만드는 <p> 태그, 줄을 바꾸는 <br> 태그 (<br>태그는 단독으로 사용하여 닫는 태그 필요 없음)
인용할 때 쓰는 <blockquote> 태그
텍스트를 굵게 강조 하려면 <strong>, 굵게 표시할 <b> 태그
이탤릭체로 강조할 <em> ,이탤릭체로 표시할 <i> 태그
```

* 예시

```html
<body>
  <div id="container">
      <h1>아메리카노</h1>
      <p>식후아메리카땡 <strong>아이스 아메리카노</strong>는 쓰다</p>
      <em>오늘은 날씨가 너무 덥네용</em>
    </div>
  </div>  
</body>
```


<img width="271" alt="스크린샷 2022-05-20 오후 2 22 49" src="https://user-images.githubusercontent.com/97012561/169456233-484aa45a-a64e-4760-8091-953039abce70.png">


* 텍스트 태그 여러 개 삽입하기 예제  
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>탐라국 입춘굿</title>
  <link rel="stylesheet" href="css/poster.css">
</head>
<body>
  <div id="container">
    <h1>탐라국 입춘굿</h1>    
    <p>탐라국 입춘굿놀이는 전국적으로 유일하게 입춘날 벌어지는 축제이자 제주도의 문화축제 중에서 유일하게 전통시대부터 존재했던 축제이다.</p>
    <p>제주에서 입춘은 새철 드는 날. <br>
      신구간이 끝나 하늘의 1만8000신이 지상으로 내려와 새해 일들을 시작하는 때다.
    </p>
    <p>자세한 정보 보기</p>
    <h2>일정</h2>
    
    <h2>먹거리</h2>
  </div>
</body>
</html>
```

 * 결과 확인하기 



<img width="478" alt="스크린샷 2022-05-19 오후 2 29 41" src="https://user-images.githubusercontent.com/97012561/169217173-55d42248-d36f-4d35-af11-c6c060cd43d5.png">
