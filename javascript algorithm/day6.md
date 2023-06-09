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



