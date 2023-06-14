## 문제 1 : 옷가게 할인 받기
### 문제 설명
머쓱이네 옷가게는 10만 원 이상 사면 5%, 30만 원 이상 사면 10%, 50만 원 이상 사면 20%를 할인해줍니다.
구매한 옷의 가격 price가 주어질 때, 지불해야 할 금액을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 10 ≤ price ≤ 1,000,000
   - price는 10원 단위로(1의 자리가 0) 주어집니다.
- 소수점 이하를 버린 정수를 return합니다.
### 입출력 예
<img width="158" alt="스크린샷 2023-06-13 오후 3 40 48" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/2a1f4053-b763-4408-8c28-8ff765ef8e5d">

### 해결 (중간)
```javascript
function solution(price) {
    if(price >= 500000) {
        return Math.floor(price*0.8);
    }
    else if(price >= 300000){
        return Math.floor(price*0.9);
    }
    else if(price >= 100000){
        return  Math.floor(price*0.95);
    }
    else return price;
  
}
```
if 문 쓸 때 500000 부터 써야 된다. 100000 부터 쓰게 되면 조건식이 성립하여 바로 100000 값만 return 하는 사실을 간과함. 주의 하자

<hr>

## 문제 2 : 아이스 아메리카노 
### 문제 설명
머쓱이는 추운 날에도 아이스 아메리카노만 마십니다. 아이스 아메리카노는 한잔에 5,500원입니다. 머쓱이가 가지고 있는 돈 money가 매개변수로 주어질 때, 머쓱이가 최대로 마실 수 있는 아메리카노의 잔 수와 남는 돈을 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 0 < money ≤ 1,000,000

### 입출력 예
<img width="161" alt="스크린샷 2023-06-13 오후 4 01 55" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/c778c997-4af5-404b-9fbb-8c4541497e2c">

### 해결 ()
```javascript
function solution(money) {
    let answer = [];
    let i = parseInt(money/5500);
    let j = money%5500;
    return answer = i,j;
}
```

<hr>

## 문제 3 : 나이 출력
### 문제 설명
머쓱이는 40살인 선생님이 몇 년도에 태어났는지 궁금해졌습니다. 나이 age가 주어질 때, 2022년을 기준 출생 연도를 return 하는 solution 함수를 완성해주세요.

### 제한사항
- 0 < age ≤ 120
- 나이는 태어난 연도에 1살이며 1년마다 1씩 증가합니다.

### 입출력 예
<img width="118" alt="스크린샷 2023-06-14 오후 12 56 57" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/f312e399-8583-491d-9e03-e03fc7c40202">

### 해결 ()
```javascript
function solution(age) {
    var answer = 0;
    return answer = 2023 - age;
}
```
