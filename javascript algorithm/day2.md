
## 문제 1 : n의 배수  

### 문제 설명
정수 num과 n이 매개 변수로 주어질 때, num이 n의 배수이면 1을 return n의 배수가 아니라면 0을 return하도록 solution 함수를 완성해주세요.

### 제한사항
2 ≤ num ≤ 100   
2 ≤ n ≤ 9  

### 입출력 예   
<img width="182" alt="스크린샷 2023-05-31 오후 3 12 33" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/fc3b18ca-4f0f-4297-beea-206c268e610a">

### 해결  
```javascript
function solution(num, n) {
    var answer = 0;
     
    if(num %n == 0) {
        answer += 1;
    }
    return answer;
}
```

<hr>

## 문제 2 : 공배수  

### 문제 설명
정수 number와 n, m이 주어집니다. number가 n의 배수이면서 m의 배수이면 1을 아니라면 0을 return하도록 solution 함수를 완성해주세요.  

### 제한사항
10 ≤ number ≤ 100  
2 ≤ n, m < 10  

### 입출력 예  
<img width="267" alt="스크린샷 2023-05-31 오후 3 27 44" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/a6976c6f-e332-4acf-9716-4388d61e40b3">

### 해결  
```
function solution(number, n, m) {
    var answer = 0;
     if(number %n == 0 && number %m == 0) {
        answer += 1;
    }
    return answer;
}
```

<hr>

## 문제 3 : 홀짝에 따라 다른 값 반환하기   

### 문제 설명
양의 정수 n이 매개변수로 주어질 때, n이 홀수라면 n 이하의 홀수인 모든 양의 정수의 합을 return 하고 n이 짝수라면 n 이하의 짝수인 모든 양의 정수의 제곱의 합을 return 하는 solution 함수를 작성해 주세요. 

### 제한사항
1 ≤ n ≤ 100  

### 입출력 예  
<img width="118" alt="스크린샷 2023-05-31 오후 3 30 27" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/1acc9b77-2769-454c-854a-32fa8805a303">

### 해결 (못함)   
```
function solution(n) {
    var answer = 0;
   

    if (n % 2 === 0) {
        for (let i = 0; i <= n; i += 1) {
            if (i % 2 === 0) answer += i ** 2;
        }
    } else {
        for (let i = 0; i <= n; i += 1) {
            if (i % 2 === 1) answer += i;
        }
    }

    return answer;
}
```

<hr>

## 문제 4 : 조건 문자열  

### 문제 설명
문자열에 따라 다음과 같이 두 수의 크기를 비교하려고 합니다.   

- 두 수가 n과 m이라면  
  - ">", "=" : n >= m  
  - "<", "=" : n <= m    
  - ">", "!" : n > m  
  - "<", "!" : n < m  

두 문자열 ineq와 eq가 주어집니다. ineq는 "<"와 ">"중 하나고, eq는 "="와 "!"중 하나입니다. 그리고 두 정수 n과 m이 주어질 때, n과 m이 ineq와 eq의 조건에 맞으면 1을 아니면 0을 return하도록 solution 함수를 완성해주세요.  


### 입출력 예  
<img width="318" alt="스크린샷 2023-05-31 오후 4 07 24" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/3eaaa0fa-2ba2-47b3-966d-a4d47050efab">

### 해결 (못함) 
```javascript
const operations = {
  '>=': (n, m) => n >= m,
  '<=': (n, m) => n <= m,
  '>!': (n, m) => n > m,
  '<!': (n, m) => n < m,
};

function solution(ineq, eq, n, m) {
  const op = operations[ineq + eq];
  return Number(op(n, m));
}
```

<hr>

## 문제 5 : flag 에 따라 다른 값 반환 하기  

### 문제 설명
두 정수 a, b와 boolean 변수 flag가 매개변수로 주어질 때, flag가 true면 a + b를 false면 a - b를 return 하는 solution 함수를 작성해 주세요.

### 제한사항  
- -1000 ≤ a, b ≤ 1,000  

### 입출력 예 
<img width="247" alt="스크린샷 2023-06-01 오전 11 56 17" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/ac278170-004f-48a6-b9ae-5ae5c50b2381">

### 해결  
```javascript
function solution(a, b, flag) {
    var answer = 0;
    
    if(flag == true) {
       answer += a + b;
    }
    else {
      answer += a-b;
    }
    return answer;
}
```

- 또 다른 풀이   
```javascript
function solution(a, b, flag) {
    return flag ? a + b : a- b;
}
```




