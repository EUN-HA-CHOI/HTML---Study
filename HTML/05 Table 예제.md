```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>table 표 - 접근성</title>
  <style>
    th,
    td {
      border: 1px solid black;
    }
  </style>
</head>

<body>
  <table summary="5개 투자회사별 매매수량, 매도수량에 대한 통계">
    <caption>코스닥선물 투자자별 매매동향</caption>
    <thead>
      <tr>
        <th rowspan="2" scope="col">구분</th>
        <th colspan="3" scope="col">매매수량</th>
        <th colspan="3" scope="col">매도수량</th>
        <th rowspan="2" scope="col">합계</th>
        <th rowspan="2" scope="col">순매수</th>
      </tr>
      <tr>
        <th scope="col">신규</th>
        <th scope="col">환매</th>
        <th scope="col">소계</th>
        <th scope="col">신규</th>
        <th scope="col">환매</th>
        <th scope="col">소계</th>
      </tr>
    </thead>
    <tfoot>
      <tr>
        <th scope="row">합계</th>
        <td>47</td>
        <td>90</td>
        <td>137</td>
        <td>6</td>
        <td>42</td>
        <td>48</td>
        <td>250</td>
        <td>24</td>
      </tr>
    </tfoot>
    <tbody>
      <tr>
        <th scope="row">선물회사</th>
        <td>47</td>
        <td>6</td>
        <td>53</td>
        <td>6</td>
        <td>42</td>
        <td>48</td>
        <td>101</td>
        <td>5</td>

      </tr>
      <tr>
        <th scope="row">증권회사</th>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>

      </tr>
      <tr>
        <th scope="row">은행</th>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>

      </tr>
      <tr>
        <th scope="row">투자신탁</th>
        <td>0</td>
        <td>84</td>
        <td>84</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>149</td>
        <td>19</td>

      </tr>
      <tr>
        <th scope="row">보험회사</th>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>

      </tr>
    </tbody>

  </table>

  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>

</body>

</html>
```

<img width="356" alt="스크린샷 2022-07-12 오후 11 28 11" src="https://user-images.githubusercontent.com/97012561/178514265-2cb9ec7a-cd12-4777-b62a-7944f6f55075.png">



```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>table- 계산기</title>
  <style>
    th,td{width: 100px; height: 100px; text-align: center;}
    th,td{border: 1px solid black;}
  </style>
</head>
<body>
  <table summary="CALCULATOP">
    <caption>CALCULATOP</caption>
    
    <tbody>
      <tr>
        <td>NUM <br /> LOCK</td>
        <td> / </td>
        <td> * </td>
        <td> - </td>
      </tr>
      <tr>
        <td>7</td>
        <td>8</td>
        <td>9</td>
        <td rowspan="2">+</td>
      </tr>
      <tr>
        <td>4</td>
        <td>5</td>
        <td>6</td>
      </tr>
      <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td rowspan="2">ENTER</td>
      </tr>
      <tr>
        <td colspan="2">0</td>
        <td>,</td>
      </tr>

    </tbody>
    
  </table>
 
</body>
</html>
```

<img width="380" alt="스크린샷 2022-07-12 오후 11 29 26" src="https://user-images.githubusercontent.com/97012561/178514606-5a208e93-014d-4b7f-81d3-50383fd6befb.png">


```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>신용등급 | 한국남부발전(주)</title>
  <style>
    th,
    td {
      border: 1px solid black;
      text-align: center;
      width: 150px;
      height: 40px;
    }

    h1 {
      text-align: center;
    }

    caption {
      text-align: left;
    }
  </style>
</head>

<body>
  <h1>신용등급</h1>
  <h2>국내외 신용등급 및 현황</h2>
  <h4>국내외 신용등급 보유현황</h4>
  <!-- 내용상 가로로 표를 나눌 때 :thead,tfoot,tbody
       내용상 세로로 표를 나눌때 : colgroup -->
       <!-- scop / id ,header  -->
  <table>
    <caption>국내외 신용등급 보유현황</caption>
    <colgroup>   <!-- 세로 열 묶을 때 -->
      <col />
    </colgroup>
    <colgroup>
      <col />
      <col />
      <col />
    </colgroup>
    <colgroup>
      <col />
      <col />
      <col />
    </colgroup>
    <thead>
      <tr>
        <th scope="col" id="division">구분</th>
        <th colspan="3" scope="col" id="domestic">국내신용등급</th>
        <th colspan="3" scope="col" id="international">국제신용등급</th>
      </tr>
    </thead>
    <!-- <tfoot></tfoot> -->
    <tbody>
      <tr>
        <th scope="row" id="agency">평가기관</th>
        <td headers="domestic agency">한국기업평가</td>
        <td headers="domestic agency">한국신용평가</td>
        <td>나이스신용평가</td>
        <td headers="international agency">Moody's</td>
        <td>S&P</td>
        <td>Fitch</td>
      </tr>
      <tr>
        <th scope="row" id="credit">신용등급</th>
        <td headers="domestic credit">AAA</td>
        <td>AAA</td>
        <td>AAA</td>
        <td headers="international credit">Aa2</td>
        <td>AA</td>
        <td>AA-</td>
      </tr>
      <tr>
        <th scope="row" id="outlook">등급전망</th>
        <td headers="domestic outloo">안정적</td>
        <td>안정적</td>
        <td>안정적</td>
        <td headers="international outlook">Stable</td>
        <td>Stable</td>
        <td>Stable</td>
      </tr>
    </tbody>
  </table>
</body>

</html>
```

<img width="600" alt="스크린샷 2022-07-12 오후 11 31 11" src="https://user-images.githubusercontent.com/97012561/178515008-943ec762-541d-49ac-adf5-4fba89bd604c.png">

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>채용공고 | 한국남부발전(주)</title>
  <style>
    th,
    tr {
      border-bottom: 1px solid black;
      border-top: 1px solid black;
    }
  </style>
</head>

<body>
  <h1>회사소개</h1>
  <p>디지털 혁신으로 친환경 에너지를 선도하는 국민기업 - 한국남부발전(주)</p>
  <h2>채용공고</h2>
  <div>총게시글<strong>25</strong>건</div>
  <table>
    <caption>채용공고</caption>
    <thead>
      <tr>
        <th scope="col" id="th-num">번호</th>
        <th scope="col" id="th-subject">제목</th>
        <th scope="col" id="th-date">작성일</th>
        <th scope="col" id="th-file">조회수</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td >25</td>
        <td ><a href="#">한국남부발전(주) 2022년 상반기 4차 기간제근로자(암모니아 운전원 및 영양사) 채용공고</a></td>
        <td >2022.06.14</td>
        <td >1762</td>
      </tr>
      <tr>
        <td >24</td>
        <td><a href="#">한국남부발전(주) 2022년 체험형 인턴 채용공고</a></td>
        <td >2022.06.14</td>
        <td >338</td>
      </tr>
      <tr>
        <td>23</td>
        <td><a href="#">솔라시도태양광발전(주) 상임이사 모집공고</a></td>
        <td>2022.06.07</td>
        <td>161</td>
      </tr>
      <tr>
        <td >22</td>
        <td><a href="#">정암풍력발전(주) 대표이사 모집공고</a></td>
        <td >2022.06.07</td>
        <td >537</td>
      </tr>
      <tr>
        <td >21</td>
        <td ><a href="#">한국남부발전(주) 2022년 사내변호사 채용공고</a></td>
        <td >2022.05.17</td>
        <td >2116</td>
      </tr>
      <tr>
        <td>20</td>
        <td><a href="#">한국남부발전(주) 2022년 상반기 3차 기간제근로자 채용공고</a></td>
        <td>2022.05.04</td>
        <td>1640</td>
      </tr>
      <tr>
        <td>19</td>
        <td><a href="#">한국남부발전(주) 2022년 상반기 2차 기간제근로자 채용공고</a></td>
        <td>2022.04.19</td>
        <td>4373</td>
      </tr>
      <tr>
        <td>18</td>
        <td><a href="#">한국남부발전(주) 2022년 전문경력직 채용공고</a></td>
        <td>2022.03.17</td>
        <td>4373</td>
      </tr>
      <tr>
        <td>17</td>
        <td><a href="#">한국남부발전(주) 2022년 상반기 기간제근로자 채용공고</a></td>
        <td>2022.03.14</td>
        <td>3432</td>
      </tr>
      <tr>
        <td >16</td>
        <td><a href="#">한국남부발전(주) 2021년 하반기 2차 기간제근로자 채용공고</a></td>
        <td >2021.11.19</td>
        <td >4147</td>
      </tr>
    </tbody>
  </table>
  <p>
    <a href="#" title="처음 페이지 이동"><img src="images/arrow-page-prev.png" alt="처음 페이지 이동">처음</a>
    <a href="#" title="이전 페이지 이동"><img src="images/arrow-prev.png" alt="이전 페이지 이동">>1</a>
    <a href="#" title="현재 페이지"></a>
    <a href="#" title="두전째 페이지"></a>
    <a href="#" title="세번째 페이지"></a>
    <a href="#" title="다음페이지"><img src="images/arrow-next.png" alt="다음 페이지 이동">다음</a>
    <a href="#" title="마지막 페이지"><img src="images/arrow-next.png" alt="마지막페이지">>끝</a>
  </p>
</body>

</html>
```
<img width="600" alt="스크린샷 2022-07-12 오후 11 34 48" src="https://user-images.githubusercontent.com/97012561/178515784-800ccb6a-f46b-41cd-9274-45f2d0e8cd06.png">

