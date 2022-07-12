```html
<!-- 회원 가입 -->

<body>
  <p><strong>*</strong>는 필수 입력 항목입니다.</p>
  <form action="/" method="post">
    <fieldset>
      <legend>회원가입양식</legend>
      <ol>
        <li>
          <label for="userId"><strong>*</strong>아이디</label>
          <input type="text" id="userId" placeholder="아이디" required autofocus />
          <input type="image" src="images/overalp.jpg" alt="중복검사" />
        </li>
        <li>
          <label for="userPw"><strong>*</strong>비밀번호</label>
          <input type="password" id="uaerPw" placeholder="비밀번호" required autofocus />
        </li>
        <li>
          <label for="phoneNum"><strong>*</strong>전화번호</label>
          <input type="tel" id="phoneNum" title="지역번호 입력" size="10" maxlength="3" /> -
          <input type="tel" title="전화번호 앞자리 입력" size="10" maxlength="4" /> -
          <input type="tel" tltle="전화번호 뒷자리 입력" size="10" maxlength="4" />
        </li>
        <li>
          <span><strong>*</strong>수신방법</span>
          <input type="radio" id="sms" />
          <label for="sms">휴대전화 sms 문자</label>

          <input type="radio" id="email" name="receive" />
          <label for="email">자주 사용하는 이메일</label>
        </li>
        <li>
          <span>메일링 리스트 가입</span>
          <input type="radio" id="yes" name="receive2" />
          <label for="yes">예</label>
          <input type="radio" id="no" name="receive2" checked />
          <label for="no">아니요</label>
        </li>
        <li>
          <label for="emailAddr">이메일</label>
          <input type="email" id="emailAddr" placeholder="이메일 아이디를 입력해주세요" /> @
          <input type="email" id="emailAddr" title="이메일 도메인명을 입력해주세요" placeholder="이메일 도메인명을 입력헤주세요" />

          <!-- label이 없는 input 타입은 title 속성 첨가 -->

          <select title="이메일 도메인 선택">
            <option value="">직접입력</option>
            <option value="gmail.com">gmail.com</option>
            <option value="naver.com">naver.com</option>
            <option value="daum.com">daum.com</option>
          </select>
        </li>
        <li>
          <label for="cell">휴대전화번호</label>
          <select id="cell">
            <option value="">직접입력</option>
            <option value="010">010</option>
            <option value="011">02</option>
          </select>
          <input type="tel" title="전화번호 앞자리 입력" maxlength="4" size="10" /> -
          <input type="tel" tltle="전화번호 뒷자리 입력" maxlength="4" size="10" />

        </li>
        <li>
          <label for="addr">주소찾기</label>
          <select id="addr">
            <option value="">선택하세요</option>
            <optgroup label="서울특별시">
              <option value="">서초구</option>
              <option value="">강남구</option>
              <option value="">종로구</option>
              <option value="">강서구</option>
            </optgroup>
            <optgroup label="경기도">
              <option value="">수원시</option>
              <option value="">안양시</option>
              <option value="">용인시</option>
              <option value="">성남시</option>
            </optgroup>
          </select>
        </li>
        <li>
          <label for="texrfield">자기소개서</label>
          <textarea cols="30" rows="5" id="texrfield">내용...</textarea>
        </li>
        <li>
          <label for="attch">첨부파일</label>
          <input type="file" id="attch" multiple />
        </li>
        <li>
          <span>취미</span>

          <input type="checkbox" id="music" />
          <label for="music">음악감상</label>

          <input type="checkbox" id="movie" />
          <label for="movie">영화감상</label>

          <input type="checkbox" id="book" />
          <label for="book">독서</label>
        </li>
        <li>
          <input type="submit" value="확인" />
          <input type="reset" value="취소" />
          <input type="button" value="버튼" />
          <input type="hidden" />
        </li>
        <li>
          <button>버튼</button>
          <button type="submit">확인</button>
          <button><img src="images/btn_search.gif"></button>
        </li>
      </ol>
    </fieldset>
  </form>
</body>
```

<img width="550" alt="스크린샷 2022-07-12 오후 11 46 49" src="https://user-images.githubusercontent.com/97012561/178518409-34ff9a57-1dcd-4507-b777-f731e678b6fd.png">


```html
<!-- 상품 주문 -->

<body>
  <form>
    <fieldset>
      <legend>개인정보입력</legend>
      <ol>
        <li>
          <label for="userName">이름</label>
          <input type="text" id="userName" value="홍길동" readonly disabled />
        </li>
        <li>
          <label for="userPw">비밀번호</label>
          <input type="passwdrd" id="userPw" placeholder="8자 이상 12자 이하, 영소문자 숫자 특수기호 포함" required autofocus
            minlength="8" maxlength="12">

        </li>
        <li>
          <label for="userPhone">전화번호</label>
          <input type="tel" id="userPhone" placeholder="02)1111-1111" required autocomplete="off" />
        </li>
      </ol>
    </fieldset>
    <fieldset>
      <legend>주문 내용</legend>
      <ol>
        <li>
          <label for="prodId">상품명</label>
          <input type="text" id="prodId">
        </li>
        <li>
          <label for="order">주문 개수</label>
          <input type="number" id="order" min="0" max="100" value="0" step="1" />
        </li>
      </ol>
    </fieldset>
    <fieldset>
      <legend>상품 검색</legend>
      <ol>
        <li>
          <label for="srch">상품 검색</label>
          <input type="search" id="srch">
        </li>
        <li>
          <label for="site">사이트 주소 입력</label>
          <input type="url" id="site" placeholder="www.abc.com">
        </li>
        <li>
          <label for="userEmail">메일 주소</label>
          <input type="email" id="uaerEmail" placeholder="example@domain.com" required />
        </li>
      </ol>
    </fieldset>
    <fieldset>
      <legend>결제 방법</legend>
      <ol>
        <li>
          <label for="cardtype">카드 선택</label>
          <input type="text" id="cardtype" list="card" />
          <datalist id="card">
            <option value="비씨카드" label="비씨카드"></option>
            <option value="국민카드" label="국민카드"></option>
            <option value="하나카드" label="하나카드"></option>
          </datalist>
        </li>
        <li>
          <label for="expired">유효기간</label>
          <input type="date" id="expired" />
          <!-- 날짜 피드: date,month,week,time,datetime-local -->
        </li>
      </ol>
    </fieldset>
    <fieldset>
      <legend>추가 선택 사항</legend>
      <ol>
        <li>
          <label for="color">색상 선택</label>
          <input type="color" id="color">
        </li>
        <li>
          <label for="slide">추가 수량 선택</label>
          <input type="range" id="slide" min="1" max="3" value="1" step="1">
        </li>
        <li>
          <label for="photo">사진 선택</label>
          <input type="file" id="photo" multiple />
        </li>
      </ol>

    </fieldset>
    <input type="submit" value="주문하기" formaction="/" formmethod="post" />
    <input type="reset" value="취소하기" />
  </form>
</body>
```

<img width="390" alt="스크린샷 2022-07-12 오후 11 49 36" src="https://user-images.githubusercontent.com/97012561/178518983-2d0ea286-bff4-4b4d-b265-0322a8b6a95a.png">

