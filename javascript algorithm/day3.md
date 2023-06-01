## 문제 1 : 코드 처리하기 

### 문제 설명
문자열 code가 주어집니다.  
code를 앞에서부터 읽으면서 만약 문자가 "1"이면 mode를 바꿉니다. mode에 따라 code를 읽어가면서 문자열 ret을 만들어냅니다.  
mode는 0과 1이 있으며, idx를 0 부터 code의 길이 - 1 까지 1씩 키워나가면서 code[idx]의 값에 따라 다음과 같이 행동합니다.  

- mode가 0일 때  
  - code[idx]가 "1"이 아니면 idx가 짝수일 때만 ret의 맨 뒤에 code[idx]를 추가합니다.  
  - code[idx]가 "1"이면 mode를 0에서 1로 바꿉니다.  
- mode가 1일 때  
  - code[idx]가 "1"이 아니면 idx가 홀수일 때만 ret의 맨 뒤에 code[idx]를 추가합니다.  
  - code[idx]가 "1"이면 mode를 1에서 0으로 바꿉니다.  

문자열 code를 통해 만들어진 문자열 ret를 return 하는 solution 함수를 완성해 주세요.
단, 시작할 때 mode는 0이며, return 하려는 ret가 만약 빈 문자열이라면 대신 "EMPTY"를 return 합니다.


### 제한사항
- 1 ≤ code의 길이 ≤ 100,000
  - code는 알파벳 소문자 또는 "1"로 이루어진 문자열입니다.  

### 입출력 예  
<img width="206" alt="스크린샷 2023-06-01 오후 12 02 09" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/75ff6bff-b972-4ce8-abfd-9d86a08d8ac0">


### 해결 (시도)
```javascript
function solution(code) {
    var answer = '';
    var mode = '0';
    
  for(let i=0; i<code.length; i++) {
     
      if(code.charAt(i) == '1') {
          mode = mode == '0' ? '1' : '0' ;
          continue;
      }
      if(mode == '0'){
          if(i%2 == 0) {
              answer += code.charAt(i);
          }
      }
      else {
        if(i%2 != 0) {
          answer += code.charAt(i);
      }  
    }
       if(answer == '') {
         answer = 'EMPTY';
      }
  }
  return  answer;
}

//12,13 라인 실패 뜸 
```

## 문제 2 : 등차수열의 특정한 항만 더하기  

### 문제 설명
두 정수 a, d와 길이가 n인 boolean 배열 included가 주어집니다. 첫째항이 a, 공차가 d인 등차수열에서 included[i]가 i + 1항을 의미할 때, 이 등차수열의 1항부터 n항까지 included가 true인 항들만 더한 값을 return 하는 solution 함수를 작성해 주세요.


### 제한사항
- 1 ≤ a ≤ 100
- 1 ≤ d ≤ 100
- 1 ≤ included의 길이 ≤ 100
- included에는 true가 적어도 하나 존재합니다.

### 입출력 예 
<img width="517" alt="스크린샷 2023-06-01 오후 1 20 27" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/f2c54b5e-298f-499b-8dd5-a2ad34fea09f">


### 해결  
```javascript
function solution(a, d, included) {
    var answer = 0;
    for (let i =0; i<included.length; i++){
        if(included[i] == true) {
            answer += a + (d*i);
        }
    }
    return answer;
}
```

<hr>

## 문제 3 : 주사위 게임 2  

### 문제설명 
1부터 6까지 숫자가 적힌 주사위가 세 개 있습니다. 세 주사위를 굴렸을 때 나온 숫자를 각각 a, b, c라고 했을 때 얻는 점수는 다음과 같습니다.

- 세 숫자가 모두 다르다면 a + b + c 점을 얻습니다.
- 세 숫자 중 어느 두 숫자는 같고 나머지 다른 숫자는 다르다면 (a + b + c) × (a2 + b2 + c2 )점을 얻습니다.
- 세 숫자가 모두 같다면 (a + b + c) × (a2 + b2 + c2 ) × (a3 + b3 + c3 )점을 얻습니다.

세 정수 a, b, c가 매개변수로 주어질 때, 얻는 점수를 return 하는 solution 함수를 작성해 주세요.


### 제한사항
- a, b, c는 1이상 6이하의 정수입니다.

### 입출력 예
<img width="265" alt="스크린샷 2023-06-01 오후 1 37 00" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/7cc6323d-83b9-42c4-9f26-161b88494593">


### 해결(못함)
```javascript 
var answer = 0;
    let one = (a + b + c) ;
    let two = (a**2+ b**2 + c**2);
    let three = (a**3 + b**3 + c**3);
    
     if(a == b && b == c ){
          answer = one * two * three;
     }
    else if (a == b || b == c || a == c) {
        answer = one * two;
    }
    else {
        answer = one; 
    }
    return answer;
```

<hr>

## 문제 4 : 원소들의 곱과 합 

### 문제 설명
정수가 담긴 리스트 num_list가 주어질 때, 모든 원소들의 곱이 모든 원소들의 합의 제곱보다 작으면 1을 크면 0을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- 2 ≤ num_list의 길이 ≤ 10
- 1 ≤ num_list의 원소 ≤ 9


### 입출력 예 
<img width="179" alt="스크린샷 2023-06-01 오후 2 40 42" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/73f98dad-424b-45ca-b1ce-b6ada2299740">

### 해결(반) 
```javascript
function solution(num_list) {
    var answer = 0;
    let sum =0 ;
    let mul =1;
    
    for(let i=0; i<num_list.length; i++){
     sum += num_list[i];
     mul *= num_list[i];
  }
    if(sum *sum > mul) {
        answer = 1;
    }
    return answer;
}
```

<hr>

## 문제 5 : 이어 붙인 수  

### 문제 설명
정수가 담긴 리스트 num_list가 주어집니다. num_list의 홀수만 순서대로 이어 붙인 수와 짝수만 순서대로 이어 붙인 수의 합을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- 2 ≤ num_list의 길이 ≤ 10
- 1 ≤ num_list의 원소 ≤ 9
- num_list에는 적어도 한 개씩의 짝수와 홀수가 있습니다.

### 입출력 예 
<img width="174" alt="스크린샷 2023-06-01 오후 2 42 06" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/3ba62fe9-275b-4fed-bc82-087ba0fc8793">


### 해결   
```javascript
function solution(num_list) {
    var answer = 0;
    let odd = '';
    let even = '';
    
    for (let i=0; i<num_list.length; i++){
        if(num_list[i]%2 == 0) {
            even += num_list[i];
        }
        else {
            odd += num_list[i];
        }
       
    }
     return Number.parseInt(even) + Number.parseInt(odd);
     
}
```

