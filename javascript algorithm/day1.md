## 알고리즘 Day_1 

## 문제_1
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

## 문제_2   
### 문제 설명
길이가 같은 두 문자열 str1과 str2가 주어집니다.  
두 문자열의 각 문자가 앞에서부터 서로 번갈아가면서 한 번씩 등장하는 문자열을 만들어 return 하는 solution 함수를 완성해 주세요.


### 제한사항
- 1 ≤ str1의 길이 = str2의 길이 ≤ 10
  - str1과 str2는 알파벳 소문자로 이루어진 문자열입니다.

### 입출력 예  
<img width="293" alt="스크린샷 2023-05-30 오후 2 13 40" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/a36e24ec-530c-4d25-880c-d559340d080d">


### 시도  
```javascript
function solution(str1, str2) {
    var answer = '';
   
    for(let i=0; i<str1.length; i++) {
        for(let j=0; j<str2.length; j++){
            answer += str1[i] + str2[j];
        }
        return answer;
    }
     
}
```

위의 코드로 작성 시 만약 `solution("fdsfa", "bbbzz");` 로 호출 하게 되면 `'fbfbfbfzfz'` 결과값이 나오므로 정답이 아니다.  
### 해결  
```javascript
function solution(str1, str2) {
    var answer = '';
    for(let i=0;i<str1.length;i++) {  
        answer += str1[i] + str2.charAt(i);  
    }
    return answer;
}
```

`charAt` 메서드를 사용함.  

<hr> 

## 문제_3  

### 문제 설명
문자들이 담겨있는 배열 arr가 주어집니다. arr의 원소들을 순서대로 이어 붙인 문자열을 return 하는 solution함수를 작성해 주세요.

### 입출력 예  
<img width="166" alt="스크린샷 2023-05-30 오후 3 12 24" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/8cc24d35-0414-4139-bead-b96929d0480f">

### 해결  
```javascript 
function solution(arr) {
    var answer = '';
    return answer += arr.join('');
} 
```

<hr>

## 문제_4 : 더 크게 합치기   

### 문제 설명
연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.  

- 12 ⊕ 3 = 123
- 3 ⊕ 12 = 312
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 b ⊕ a 중 더 큰 값을 return 하는 solution 함수를 완성해 주세요.  

단, a ⊕ b와 b ⊕ a가 같다면 a ⊕ b를 return 합니다.  

### 제한사항  
- 1 ≤ a, b < 10,000  

### 입출력 예   
<img width="187" alt="스크린샷 2023-05-30 오후 3 16 11" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/5df5b275-51d7-47e7-96db-f9743d2f85f7">  

### 해결  
```javascript 
function solution(a, b) {
    var answer = '';
    var num = String;   
    if(num(a) + num(b) > num(b) + num(a)) {
        answer += num(a) + num(b)
    }
    else {
        answer += num(b) + num(a)
    }
    return  parseInt(answer);
    
}
```


<hr>

## 문제_5 : 두 수의 연산값 비교하기  

### 문제 설명
연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.  

- 12 ⊕ 3 = 123  
- 3 ⊕ 12 = 312  
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 2 * a * b 중 더 큰 값을 return하는 solution 함수를 완성해 주세요.  

단, a ⊕ b와 2 * a * b가 같으면 a ⊕ b를 return 합니다.  


### 입출력 예  
<img width="181" alt="스크린샷 2023-05-30 오후 3 56 31" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/7f0fc95c-1ae1-4c03-951f-17596688b021">

### 해결  
```javascript 
function solution(a, b) {
    var answer = '';
    var num = String;   
    if(num(a) + num(b) > 2 * num(a) * num(b)) {
        answer += num(a) + num(b)
    }
    else {
        answer += 2 * num(a) * num(b)
    }
    return  parseInt(answer);
    
}
```



