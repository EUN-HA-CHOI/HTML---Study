## 표 만들기  
### 표의 구성 요소 알아보기
*표는 행과 열 그리고 셀로 이루어짐  
*표 제목 : capstion / 표 전체 : table / 행 : tr / 셀 : td / 제목 셀 : th

``` html 
표를 만드는 <table> , <caption> 태그

  기본형 -> <table>
             <caption>표 제목</caption>
          </table>
``` 
* 예시 
``` html
<head>
  <meta charset="UTF-8">
  <title>상품 소개 페이지</title>
  <style>
    table, th, td {
      border:1px solid #ccc;
      border-collapse: collapse;
    }
    th, td { padding: 10px 20px; }
  </style>
   
</head>
<body>
  <table>
    <caption>커피</caption>
    <thead>
      <tr>
        <th>에스프레소</th>
        <th>아메리카노</th>
        <th>카푸치노</th> 
        <th>카페라떼</th>   
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>곱게 간 원두 가루에 뜨거운 물로 뽑아낸 커피</td>
        <td>에스프레소에 물을 넣어 연하게 마시는 커피</td>
        <td>우유를 섞은 커피에 계핏가루를 뿌린 커피</td>
        <td>카페라떼는 우유를 이용한 커피</td>
      </tr>
    </tbody>
  </table>
</body>
```
<img width="490" alt="스크린샷 2022-05-20 오후 4 08 25" src="https://user-images.githubusercontent.com/97012561/169472909-39eba8ef-8377-4ac4-8b54-647cecb2f394.png">



### 표를 만드는 tr 태그와 셀을 만드는 td , th 태그 
```html 
표를 만드는 <tr> 태그와 셀을 만드는 <td> , <th> 태그 

  기본형 -> <table>
             <tr>
               <td>1행 1열</td>
               <td>1행 2열</td>
             </tr>
             <tr>
               <td>1행 1열</td>
               <td>1행 2열</td>
             </tr>
          </table>
```


### 표의 구조를 지정하는 thead , tbody , tfoot 태그  
*제목셀 자료셀 표 아래쪽이 있는 표는 제목 , 본문 , 요약이 있는 부분으로 표의 구조를 누는 것이 좋음.
```html
<!--생략-->
  <h2>상품 구성</h2>
  <table>
    <caption>선물용과 가정용 상품 구성</caption>
    <thead>
      <tr>
        <th>용도</th>
        <th>중량</th>
        <th>갯수</th>
        <th>가격</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>선물용</td>
        <td>3kg</td>
        <td>11~16과</td>
        <td>35,000원</td>
      </tr>
      <tr>
        <td>선물용</td>
        <td>5kg</td>
        <td>18~26과</td>
        <td>52,000원</td>
      </tr>
      <tr>
        <td>가정용</td>
        <td>3kg</td>
        <td>11~16과</td>
        <td>30,000원</td>
      </tr>   
      <tr>
        <td>가정용</td>
        <td>5kg</td>
        <td>18~26과</td>
        <td>47,000원</td>
      </tr>
    </tbody>        
  </table>
```

* 결과 
<img width="362" alt="스크린샷 2022-05-19 오후 4 41 49" src="https://user-images.githubusercontent.com/97012561/169239744-7e6a7494-c2c5-4ebb-bc25-d43387cd6ce8.png"> 

*용도,중량,개수,가격이 thead 태그 / 바로 밑 전체 칸이 tbody  

### 행을 합치려면 rowspan , 열을 합치려면 colspan 속성
``` html
 기본형 -> <td rowspan="합칠 셀의 개수">셀의 내용</td>
         <td colspan="합칠 셀의 개수">셀의 내용</td>

 <table>
    <caption>선물용과 가정용 상품 구성</caption>
    <thead>
      <tr>
        <th>용도</th>
        <th>중량</th>
        <th>갯수</t>
        <th>가격</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td rowspan="2">선물용</td>    <!--2개의 행 합치기-->
        <td>3kg</td>
        <td>11~16과</td>              <!--3개의 셀만 작성-->
        <td>35,000원</td>
      </tr>
      <tr>
        <td>5kg</td>
        <td>18~26과</td>
        <td>52,000원</td>
      </tr>
      <tr>
        <td rowspan="2">가정용</td>   <!--2개의 행 합치기-->
        <td>3kg</td>
        <td>11~16과</td>             <!--3개의 셀만 작성-->
        <td>30,000원</td>
      </tr>   
      <tr>
        <td>5kg</td>
        <td>18~26과</td>
        <td>47,000원</td>
      </tr>
    </tbody>        
  </table>
```

* 결과
<img width="370" alt="스크린샷 2022-05-19 오후 4 53 26" src="https://user-images.githubusercontent.com/97012561/169242044-a0d30e39-34ec-43e8-883e-8099b94804c2.png">

### 열을 묶어 주는 col , colgroup 태그 , 스타일 꾸미기 가능
```html


  기본형 -> <colgroup>     <!--<colgroup>는 <col>태그를 2개 이상 묶어서 사용-->
              <col>      <!-- <col>태그는 열을 1개만 지정할 때 -->
          </colgroup>
```  

* 예시 
```html
<caption>커피</caption>
    <colgroup>
    <col style="background-color:#eee"; >
    </colgroup>
```
<img width="509" alt="스크린샷 2022-05-20 오후 4 54 38" src="https://user-images.githubusercontent.com/97012561/169481182-6959168b-df35-4fd8-9766-0da55abd93a0.png">





