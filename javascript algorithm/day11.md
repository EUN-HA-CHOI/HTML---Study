## 문제 1 : 문자 반복 출력하기  

### 문제 설명
문자열 my_string과 정수 n이 매개변수로 주어질 때, my_string에 들어있는 각 문자를 n만큼 반복한 문자열을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 2 ≤ my_string 길이 ≤ 5
- 2 ≤ n ≤ 10
- "my_string"은 영어 대소문자로 이루어져 있습니다.


### 입출력 예 
<img width="280" alt="스크린샷 2023-06-15 오후 2 12 27" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/822a7c4a-fa2a-42f9-b776-36a1912523c6">

### 입출력 예 설명 
- "hello"의 각 문자를 세 번씩 반복한 "hhheeellllllooo"를 return 합니다.

### 해결 
```javascript
function solution(my_string, n) {
    var answer = '';
    for(let i=0; i<my_string.length; i++){
       answer += my_string[i].repeat(n);
    }
    return answer;
}
```

<hr>

## 문제 2 : 특정 문자 제거하기   

### 문제 설명
문자열 my_string과 문자 letter이 매개변수로 주어집니다. my_string에서 letter를 제거한 문자열을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- 1 ≤ my_string의 길이 ≤ 100
- letter은 길이가 1인 영문자입니다.
- my_string과 letter은 알파벳 대소문자로 이루어져 있습니다.
- 대문자와 소문자를 구분합니다.

### 입출력 예 
<img width="238" alt="스크린샷 2023-06-15 오후 2 27 45" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/922b371f-c449-4a37-8a1d-92962e6f9b77">

### 입출력 예 설명 
- "abcdef" 에서 "f"를 제거한 "abcde"를 return합니다.
- "BCBdbe" 에서 "B"를 모두 제거한 "Cdbe"를 return합니다.

### 해결 
```javascript
function solution(my_string, letter) {
    var answer = '';
    for(let i=0; i<my_string.length; i++){
        answer += my_string[i].replace(letter,'');
    }
    return answer;
}

// function solution(my_string, letter) {
//    return my_string.replace(letter, '');
//  }
```

- 또 다른 방법
```javascript
function solution(my_string, letter) {
    var answer = '';
    for(let i=0; i<my_string.length; i++){
        if(my_string[i] !== letter){
   answer +=my_string[i];
       }
    }
    return answer;
}
```

<hr>

## 문제 3 : 각도기

### 문제 설명
각에서 0도 초과 90도 미만은 예각, 90도는 직각, 90도 초과 180도 미만은 둔각 180도는 평각으로 분류합니다. 각 angle이 매개변수로 주어질 때 예각일 때 1, 직각일 때 2, 둔각일 때 3, 평각일 때 4를 return하도록 solution 함수를 완성해주세요.

- 예각 : 0 < angle < 90
- 직각 : angle = 90
- 둔각 : 90 < angle < 180
- 평각 : angle = 180

### 제한사항
- 0 < angle ≤ 180
- angle은 정수입니다.

### 입출력 예 
<img width="122" alt="스크린샷 2023-06-15 오후 2 43 50" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/0504ad7a-c495-4290-9531-be19df3164cc">


### 입출력 예 설명 
- angle이 70이므로 예각입니다. 따라서 1을 return합니다.
- angle이 91이므로 둔각입니다. 따라서 3을 return합니다.
- angle이 180이므로 평각입니다. 따라서 4를 return합니다.

### 해결 
```javascript

```

<hr>
