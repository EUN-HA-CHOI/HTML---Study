
```html
<body>
  <!-- html5 시멘틱 웹 [semantic web] : 의미가 더 명확해진다. 
   header, footer, nav, section, article, aside
  -->
  <div id="wrap">
    <header>
      <h1>제목</h1>
      <h2>부제목</h2>
      <nav class="gnb">
        <h2>주메뉴</h2>
      <ul>
        <li><a href="#">메뉴</a></li>
        <li><a href="#">메뉴</a></li>
        <li><a href="#">메뉴</a></li>
        <li><a href="#">메뉴</a></li>
      </ul>
      </nav>
      
    </header>
    <main>
      <nav class="snb">
        <h2>제목</h2>
        <ul>
          <li><a href="#">메뉴</a></li>
          <li><a href="#">메뉴</a></li>
          <li><a href="#">메뉴</a></li>
          <li><a href="#">메뉴</a></li>
        </ul>
      </nav>
      <div id="content">
        <section class="notice">
          <h3>공지사항</h3>
          <ul>
            <li><a href="#">글 제목</a></li>
            <li><a href="#">글 제목</a></li>
            <li><a href="#">글 제목</a></li>
          </ul>
          <p>공지사항 더보기</p>
        </section>
        <section class="notice">
          <h3>자료실</h3>
          <ul>
            <li><a href="#">글 제목</a></li>
            <li><a href="#">글 제목</a></li>
            <li><a href="#">글 제목</a></li>
          </ul>
          <p>자료실 더보기</p>
        </section>
        <article>
          <h3>제목</h3>
          <p>기사글,블로그글,게시판글</p>
        </article>
      </div>
    </main>
    <aside  class="quick_menu">
      <!-- 퀵메뉴 -->
      <h3>바로가기</h3>
      <ul>
        <li><a href="#">퀵 메뉴</a></li>
        <li><a href="#">퀵 메뉴</a></li>
        <li><a href="#">퀵 메뉴</a></li>
      </ul>
    </aside>
    <footer>copyright(c)</footer>
  </div>
</body>
```
