## input 태그의 주요 속성
### 자동으로 입력 커서를 갖다 놓는 autofocus 속성 
*autofocus 속성을 사용하면 페이지를 불러오자마자 폼에서 원하는 요소에 마우스 포인터 표시 가능.
```html
기본형 -> <input type=텍스트-입력-필드 autofocus required>

 <li>
   <label for="user-name">이름 </label>
   <input type="text" id="user-name" autofocus required>
 </li>

```

### 힌트를 표시해 주는 placeholder 속성
```html
<li>
  <label for="phone">연락처</label>
  <input type="tel" id="phone" placeholder="하이픈 빼고 입력해 주세요.(01012345678)" required>
</li>
```
<img width="483" alt="스크린샷 2022-05-23 오후 3 50 14" src="https://user-images.githubusercontent.com/97012561/169760257-04b84823-bfac-425c-af63-bb6ea10fd5a2.png">


### 읽기 전용 필드를 만들어 주는 readonly 속성
```html
기본형 -> <input type=텍스트-입력-필드 readonly>

<li>
  <label for="prod">주문 상품</label>
  <input type="text" id="prod" value="상품용 3KG" readonly>
</li>
```

### 필수 입력 필드를 지정하는 required 속성 

``` html
<li>
   <label for="user-name">이름 </label>
   <input type="text" id="user-name" autofocus required>
 </li>
```
<img width="493" alt="스크린샷 2022-05-23 오후 3 57 13" src="https://user-images.githubusercontent.com/97012561/169761438-61e6b763-8001-44be-af88-6647e78dcd76.png">


