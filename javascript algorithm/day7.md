## 문제 1 : 배열 두 배 만들기  

### 문제 설명
정수 배열 numbers가 매개변수로 주어집니다. numbers의 각 원소에 두배한 원소를 가진 배열을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- -10,000 ≤ numbers의 원소 ≤ 10,000
- 1 ≤ numbers의 길이 ≤ 1,000

### 입출력 예
<img width="376" alt="스크린샷 2023-06-12 오전 11 44 51" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/b486daf2-5ab8-4a5b-b94a-cfbb263ce69e">

### 해결
```javascript
function solution(numbers) {
    var answer = [];
    for(let i=0; i<numbers.length; i++){
      answer.push(numbers[i]*2);
    }
    return answer;
}
```

<hr>

## 문제 2 : 나머지 구하기

### 문제 설명
정수 num1, num2가 매개변수로 주어질 때, num1를 num2로 나눈 나머지를 return 하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

### 입출력 예
<img width="191" alt="스크린샷 2023-06-12 오전 11 52 05" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/cabe7472-f220-4900-b8e1-a789df926c62">


### 해결
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer = num1%num2;
}
```

<hr>

## 문제 3 : 중앙값 구하기

### 문제 설명
중앙값은 어떤 주어진 값들을 크기의 순서대로 정렬했을 때 가장 중앙에 위치하는 값을 의미합니다. 예를 들어 1, 2, 7, 10, 11의 중앙값은 7입니다. 정수 배열 array가 매개변수로 주어질 때, 중앙값을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- array의 길이는 홀수입니다.
- 0 < array의 길이 < 100
- -1,000 < array의 원소 < 1,000

### 입출력 예
<img width="182" alt="스크린샷 2023-06-12 오전 11 56 40" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/8c020493-70a5-4345-8c04-7f7786eea6ea">

### 해결
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer = num1%num2;
}
```
