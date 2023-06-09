## 문제 1 : 두 수의 합 

### 문제 설명
정수 num1과 num2가 주어질 때, num1과 num2의 합을 return하도록 soltuion 함수를 완성해주세요.

### 제한사항
- -50,000 ≤ num1 ≤ 50,000
- -50,000 ≤ num2 ≤ 50,000


### 입출력 예
<img width="184" alt="스크린샷 2023-06-09 오후 5 00 19" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/57bce4e0-2a74-45ea-85a6-d8d81790da02">

### 해결 
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer += num1 + num2  ;
}
```

<hr>

## 문제 2 : 두 수의 차

### 문제 설명
정수 num1과 num2가 주어질 때, num1에서 num2를 뺀 값을 return하도록 soltuion 함수를 완성해주세요.

### 제한사항
- -50,000 ≤ num1 ≤ 50,000
- -50,000 ≤ num2 ≤ 50,000


### 입출력 예
<img width="193" alt="스크린샷 2023-06-09 오후 5 58 02" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/498c132c-0c98-4833-8a00-569ef101eace">


### 해결 
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer += num1 - num2  ;
}
```

<hr>

## 문제 3 : 두 수의 곱

### 문제 설명
정수 num1, num2가 매개변수 주어집니다. num1과 num2를 곱한 값을 return 하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 ≤ num1 ≤ 100
- 0 ≤ num2 ≤ 100


### 입출력 예
<img width="180" alt="스크린샷 2023-06-09 오후 5 59 16" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/ce0c7880-9a05-466f-84c4-07da5c439b9e">

### 해결 
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer += num1 * num2  ;
}
```

<hr>

## 문제 4 : 몫 구하기

### 문제 설명
정수 num1, num2가 매개변수로 주어질 때, num1을 num2로 나눈 몫을 return 하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 ≤ num1 ≤ 100
- 0 ≤ num2 ≤ 100


### 입출력 예
<img width="190" alt="스크린샷 2023-06-09 오후 6 00 33" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/4c7a8113-f2c4-416a-9f08-7b0b9253fb8c">


### 해결 
```javascript
function solution(num1, num2) {
    var answer =Math.floor(num1/num2) ;
    return answer ;
}
```

<hr>

## 문제 5 : 두 수의 나눗셈

### 문제 설명
정수 num1과 num2가 매개변수로 주어질 때, num1을 num2로 나눈 값에 1,000을 곱한 후 정수 부분을 return 하도록 soltuion 함수를 완성해주세요.

### 제한사항
- 0 ≤ num1 ≤ 100
- 0 ≤ num2 ≤ 100


### 입출력 예
<img width="188" alt="스크린샷 2023-06-09 오후 6 29 38" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/3dcda7cf-604b-4664-b93e-0f33f89fec04">

### 해결 
```javascript
function solution(num1, num2) {
    var answer = num1/num2;
    return Math.floor(answer * 1000);
}
```

<hr>

## 문제 6 : 숫자 비교하기 

### 문제 설명
정수 num1과 num2가 매개변수로 주어집니다. 두 수가 같으면 1 다르면 -1을 retrun하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 ≤ num1 ≤ 10,000
- 0 ≤ num2 ≤ 10,000


### 입출력 예
<img width="183" alt="스크린샷 2023-06-09 오후 6 36 26" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/047309a0-16ab-4c28-b34f-ad424f0cdf02">


### 해결 
```javascript
function solution(num1, num2) {
    var answer = 0;
    if(num1 === num2) {
        answer = 1;
    }else {
        answer = -1
    }
    return answer;
}
```

<hr>

## 문제 7 : 분수의 덧셈

### 문제 설명
첫 번째 분수의 분자와 분모를 뜻하는 numer1, denom1, 두 번째 분수의 분자와 분모를 뜻하는 numer2, denom2가 매개변수로 주어집니다. 두 분수를 더한 값을 기약 분수로 나타냈을 때 분자와 분모를 순서대로 담은 배열을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 0 <numer1, denom1, numer2, denom2 < 1,000

### 입출력 예
<img width="396" alt="스크린샷 2023-06-09 오후 6 39 07" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/ca8c14fc-8754-4717-90fe-7c5f1df89534">


### 해결 
```javascript
// 최대 공약수 구하기
function cal_gcd(a, b) {
    return a % b === 0 ? b : cal_gcd(b, a % b)
}

function solution(denum1, num1, denum2, num2) {
    let denum = denum1 * num2 + denum2 * num1;
    let num = num1 * num2;
    let gcd = cal_gcd(denum, num);
    
    // 최대 공약수를 분자 분모에 나누고 배열에 넣기
    return [denum / gcd, num / gcd]
}
```





