## 하이퍼링크 삽입하기 

### 링크를 삽입하는 a 태그와 href 속성  
```html 
기본형 -> <a href="링크할 주소">텍스트 또는 이미지</a>

*텍스트 링크 만들기 : href 속성에는 텍스트를 클릭하면 연결할 문서의 경로와 파일명을 넣으면 된다.


* 예시1 
``` html 
<p><a href="링크할 주소">주문서 작성하기</a></p>

<div>
  <p><a href="../05/order.html">주문서 작성하기</a></p>
</div>

 <p>
  <a href="한국형 웹 콘텐츠 접근성 지침 2.1.pdf" target="_blank" title="새창">한국형 웹 콘텐츠 접근성 지침 2.1 내려받기</a>
</p>

```

<img width="393" alt="스크린샷 2022-05-23 오후 2 29 00" src="https://user-images.githubusercontent.com/97012561/169749593-d8b2c05a-7d07-47da-b65b-6595e5b88e67.png">

<img width="384" alt="스크린샷 2022-05-23 오후 2 29 20" src="https://user-images.githubusercontent.com/97012561/169749647-c020582f-c512-4305-8dc1-941f77f443a3.png">

* 예시2

``` html 
*링크를 새 탭에서 열어 주는 target 속성 
<p><a href="링크할 주소" target="_blank">주문서 작성하기</a></p>

<div>
  <p><a href="../05/order.html" target="_blank">주문서 작성하기</a></p>
</div>
```

<img width="593" alt="스크린샷 2022-05-23 오후 2 31 13" src="https://user-images.githubusercontent.com/97012561/169749864-e38ea35c-deb8-4e2f-a388-c415a6e4ec3f.png">
