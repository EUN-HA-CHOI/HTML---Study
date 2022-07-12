### 목록 만들기  
```html
순서 있는 목록을 만드는 <ol> , <li> 태그  
<!-- ol 태그 안에는 li만 가능ㄴ -->
   기본형 -> <ol>
             <li>항목1</li>
             <li>항목2</li>
            </ol>
```  
##### *순서 있는 목록은 type 속성을 이용하여 순서를 나타낸다.  (start 속성을 사용하여 시작 번호를 바꿀 수 있다.)  
| 종류 | 설명 |
|----|----|
|type = "1" | 숫자 |
|type = "a" |영문 소문자|
|type = "i" |로마숫자 소|  

```html  
순서 없는 목록을 만드는 <ul> , <li> 태그  

  기본형 -> <ul>
            <li>항목1</li>
            <li>항목2</li>
          </ul>
<!-- ex -->
<div>
  <h2>공지사항</h2>
  <ul>
    <li><a href="#">[홍보] 2022 국민행복 IT 경진...</a><span>2022-07-05</span></li>
    <li><a href="#">2022년 제2차 정보접근성 오픈 아..</a><span>2022-06-16</span></li>
    <li><a href="#">2022년 제1차 정보접근성 오픈 아...</a><span>2022-03-23</span></li>
    <li><a href="#">2021년 제4차 정보접근성 오픈 아...</a><span>2022-11-24</span></li>
  </ul>
  <p><a href="#"><img src="images/btn_more.gif" alt="공지사항 더보기"></a></p>
 </div>
```  
<img width="250" alt="스크린샷 2022-07-12 오후 11 09 26" src="https://user-images.githubusercontent.com/97012561/178510072-482cfe4e-6e06-4f83-a737-5686df946c12.png">


``` html
설명 목록을 만드는 <dl> , <dt> , <dd> 태그 

  기본형 -> <dl>             
            <dt>이름</dt>  
            <dd></dd>    <!--<dt> 사이에 <dd> 여러 개 사용 가능-->
          </dl>

<!--  ex  -->
<h1><a href="#">NHN</a></h1>
<h2>회사소개</h2>
<h3>Location</h3>
<dl>
  <dt>address</dt>
  <dd>13487 경기도 성남시 분당구 대왕판교로645번길 16 NHN 플레이뮤지엄</dd>
  <dd>NHN Play Museum, 16 Daewangpangyo-ro 645beon-gil, Bundang-gu, Seongnam-si,     Gyeonggi-do, 13487,   Korea</dd>
  <dt>TEL</dt>
  <dd>1544-6859 (ARS)</dd>
  <dt>FAX</dt>
  <dd>031-8038-3000</dd>
  <dt>사업자번호</dt>
  <dd>144-81-15549</dd>
</dl>
```  
<img width="280" alt="스크린샷 2022-07-12 오후 11 22 41" src="https://user-images.githubusercontent.com/97012561/178513067-a2dd8022-9c46-407f-ab0e-c06b1ab4afd8.png">


* 예시
``` html
<dl>
    <dt>아이스 아메리카노</dt>
    <dd>:에스프레소에 뜨거운 물을 희석시켜 만든 음료</dd> 
</dl>

```
<img width="332" alt="스크린샷 2022-05-20 오후 3 05 10" src="https://user-images.githubusercontent.com/97012561/169463418-546de38c-d7f9-435d-bbf6-f619231eef37.png">
