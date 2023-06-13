## 문제 1 : 피자 나눠먹기 (1)

### 문제 설명
머쓱이네 피자가게는 피자를 일곱 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 n이 주어질 때, 모든 사람이 피자를 한 조각 이상 먹기 위해 필요한 피자의 수를 return 하는 solution 함수를 완성해보세요.

### 제한사항
- 1 ≤ n ≤ 100

### 입출력 예
<img width="120" alt="스크린샷 2023-06-13 오전 11 02 34" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/fc0a93ec-b4df-4210-b542-be147ac557af">

### 입출력 예 설명 
 
- 7명이 최소 한 조각씩 먹기 위해서 최소 1판이 필요합니다.
 
- 1명은 최소 한 조각을 먹기 위해 1판이 필요합니다.
  
- 15명이 최소 한 조각씩 먹기 위해서 최소 3판이 필요합니다.

### 해결
```javascript
function solution(n) {
    var answer = Math.ceil(n / 7);
    if(answer >= 1) {
      return answer;
    } 
}
```

<hr>

## 문제 2 : 피자 나눠먹기 (2)

### 문제 설명
머쓱이네 피자가게는 피자를 여섯 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 n이 매개변수로 주어질 때, n명이 주문한 피자를 남기지 않고 모두 같은 수의 피자 조각을 먹어야 한다면 최소 몇 판을 시켜야 하는지를 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 1 ≤ n ≤ 100

### 입출력 예
<img width="120" alt="스크린샷 2023-06-13 오전 11 09 03" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/7704791a-3772-40ea-a04e-2617ad3e0c0e">

### 입출력 예 설명 
 
- 6명이 모두 같은 양을 먹기 위해 한 판을 시켜야 피자가 6조각으로 모두 한 조각씩 먹을 수 있습니다.
 
- 10명이 모두 같은 양을 먹기 위해 최소 5판을 시켜야 피자가 30조각으로 모두 세 조각씩 먹을 수 있습니다.
  
- 4명이 모두 같은 양을 먹기 위해 최소 2판을 시키면 피자가 12조각으로 모두 세 조각씩 먹을 수 있습니다.

### 해결(x)
```javascript
function solution(n) {
    let answer = 6;
    while(answer%n !== 0) {
         answer += 6;
    }
    return answer/6;
}
```

<hr>

## 문제 3 : 피자 나눠먹기 (3)

### 문제 설명
머쓱이네 피자가게는 피자를 두 조각에서 열 조각까지 원하는 조각 수로 잘라줍니다. 피자 조각 수 slice와 피자를 먹는 사람의 수 n이 매개변수로 주어질 때, n명의 사람이 최소 한 조각 이상 피자를 먹으려면 최소 몇 판의 피자를 시켜야 하는지를 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 2 ≤ slice ≤ 10
- 1 ≤ n ≤ 100

### 입출력 예
<img width="181" alt="스크린샷 2023-06-13 오후 12 01 35" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/865ba557-f5b2-44cf-b21b-f6584b0605a3">

### 입출력 예 설명 
 
- 10명이 7조각으로 자른 피자를 한 조각 이상씩 먹으려면 최소 2판을 시켜야 합니다.
 
- 12명이 4조각으로 자른 피자를 한 조각 이상씩 먹으려면 최소 3판을 시켜야 합니다.
  
### 해결(x)
```javascript
function solution(slice, n) {
    if(n % slice === 0){
        return n / slice
    }else{
        return parseInt(n / slice) + 1
    }
}
```

<hr>

## 문제 4 : 배열의 평균값

### 문제 설명
정수 배열 numbers가 매개변수로 주어집니다. numbers의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 ≤ numbers의 원소 ≤ 1,000
- 1 ≤ numbers의 길이 ≤ 100
- 정답의 소수 부분이 .0 또는 .5인 경우만 입력으로 주어집니다.

### 입출력 예
<img width="367" alt="스크린샷 2023-06-13 오후 12 40 42" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/f36e1257-c264-41cf-9936-1c21f067b522">

### 입출력 예 설명 
- numbers의 원소들의 평균 값은 5.5입니다.
 
- numbers의 원소들의 평균 값은 94.0입니다.
  
### 해결
```javascript
function solution(numbers) {
    var answer = 0;
    return answer = numbers.reduce((a,b) => a + b) / numbers.length;
}
```
