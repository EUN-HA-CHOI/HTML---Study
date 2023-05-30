## 알고리즘 Day_1 

## 문제 1
### 문제 설명  
문자열 my_string, overwrite_string과 정수 s가 주어집니다. 문자열 my_string의 인덱스 s부터 overwrite_string의 길이만큼을 문자열 overwrite_string으로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.  

### 제한사항
- my_string와 overwrite_string은 숫자와 알파벳으로 이루어져 있습니다.  
- 1 ≤ overwrite_string의 길이 ≤ my_string의 길이 ≤ 1,000  
- 0 ≤ s ≤ my_string의 길이 - overwrite_string의 길이  

### 입출력 예  
<img width="543" alt="스크린샷 2023-05-30 오후 1 54 04" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/3be35a30-bcb8-446b-8032-1d3e44fde9b4">

### 해결  
```javascript
function solution(my_string, overwrite_string, s) {
    var answer = '';
    return my_string.slice(0,s) + overwrite_string + my_string.slice(s+overwrite_string.length);
}
```

### 결과  
<img width="413" alt="스크린샷 2023-05-30 오후 1 55 30" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/57c600ab-7375-4898-aad0-6f54c83017da">

<hr> 

## 문제2   
