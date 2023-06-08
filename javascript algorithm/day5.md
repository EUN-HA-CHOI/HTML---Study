## 문제 1 : 수 조작하기 1  

### 문제 설명
정수 n과 문자열 control이 주어집니다. control은 "w", "a", "s", "d"의 4개의 문자로 이루어져 있으며, control의 앞에서부터 순서대로 문자에 따라 n의 값을 바꿉니다.

- "w" : n이 1 커집니다.
- "s" : n이 1 작아집니다.
- "d" : n이 10 커집니다.
- "a" : n이 10 작아집니다.
위 규칙에 따라 n을 바꿨을 때 가장 마지막에 나오는 n의 값을 return 하는 solution 함수를 완성해 주세요.

### 제한사항
- -100,000 ≤ n ≤ 100,000
- 1 ≤ control의 길이 ≤ 100,000
  - control은 알파벳 소문자 "w", "a", "s", "d"로 이루어진 문자열입니다.

### 입출력 예  
<img width="273" alt="스크린샷 2023-06-08 오전 11 19 43" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/07048880-b213-4b91-87e0-4ca4976ad358">


### 해결(x)
```javascript
function solution(n, control) {
    const controller = {
        w:1,
        s:-1,
        d:10,
        a:-10
    }
    return [...control].reduce((acc, cur)=>acc + controller[cur], n);
}
```

### reduce 메서드    
배열의 여러개의 값을 하나의 값으로 축소    

`array.reduce(콜백함수, 초기값)`

reduce 메서드는 고차 함수이다. 첫번째 인수 자리에 콜백함수가 들어온다. 두번째 인수자리(생략가능) 에는 초기값이 들어온다.  
reduce 메서드는 자신을 호출한 배열의 모든 요소를 순회하며 인수로 전달받은 콜백함수를 반복 호출한다. 이때 원본 배열은 변경 되지 않는다.  

일반적으로 reduce 메서드는 배열 요소들의 평균을 구할 때 많이 쓴다.

- 예시  
```javascript
const array1 = [20, 35, 1, 98, 46, 5];
array1.reduce((a, b) => (a + b)) / array1.length; 
//결과 : 205
```

위의 표현식은 (20 + 35 + 1 + 98 + 46 + 5 ) / array.length 를 계산한 것과 같다.  
그렇다면 어떻게 위의 결과가 나오는지 순서대로 하나씩 확인 해 보자.  

```javascript
(1) a : 20, b : 35
(2) a : 55(20 + 35), b : 1
(3) a : 56(20 + 35 + 1), b : 98
(4) a : 154(20 + 35 + 1 + 98), b : 46
(5) a : 200(20 + 35 + 1 + 98 + 46), b : 5
(6) array1.reduce((a, b) => (a + b)) 에서 return 되는 값 = a + b = 205 
(7) 205 / 6 = 34.166666666666664
```

<hr>

## 문제 2 : 수 조작하기 2

### 문제설명
정수 배열 numLog가 주어집니다. 처음에 numLog[0]에서 부터 시작해 "w", "a", "s", "d"로 이루어진 문자열을 입력으로 받아 순서대로 다음과 같은 조작을 했다고 합시다.

- "w" : 수에 1을 더한다.
- "s" : 수에 1을 뺀다.
- "d" : 수에 10을 더한다.
- "a" : 수에 10을 뺀다.
그리고 매번 조작을 할 때마다 결괏값을 기록한 정수 배열이 numLog입니다. 즉, numLog[i]는 numLog[0]로부터 총 i번의 조작을 가한 결과가 저장되어 있습니다.

주어진 정수 배열 numLog에 대해 조작을 위해 입력받은 문자열을 return 하는 solution 함수를 완성해 주세요.

### 제한사항
- 2 ≤ log의 길이 ≤ 100,000
  - -100,000 ≤ log[0] ≤ 100,000
  - 1 ≤ i ≤ log의 길이인 모든 i에 대해 |log[i] - log[i - 1]|의 값은 1 또는 10입니다.
  
### 입출력 예  
<img width="413" alt="스크린샷 2023-06-08 오후 12 58 18" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/29cb357b-35ed-4b15-91d1-408b8e2bb0d3">

### 해결(x)
```javascript
function solution(numLog) {
    const controller = {
        "1":"w",
        "-1":"s",
        "10":"d",
        "-10":"a"
    }
    return numLog.slice(1).reduce((acc, cur, idx)=>acc + controller[`${numLog[idx+1]-numLog[idx]}`],"");
}
```


<hr>

## 문제 3 : 수열과 구간 쿼리 3

### 문제설명 
정수 배열 arr와 2차원 정수 배열 queries이 주어집니다. queries의 원소는 각각 하나의 query를 나타내며, [i, j] 꼴입니다.
각 query마다 순서대로 arr[i]의 값과 arr[j]의 값을 서로 바꿉니다.
위 규칙에 따라 queries를 처리한 이후의 arr를 return 하는 solution 함수를 완성해 주세요.
 
### 제한사항
- 1 ≤ arr의 길이 ≤ 1,000
  - 0 ≤ arr의 원소 ≤ 1,000,000
- 1 ≤ queries의 길이 ≤ 1,000
  - 0 ≤ i < j < arr의 길이

### 입출력 예
<img width="380" alt="스크린샷 2023-06-08 오후 2 26 03" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/57076784-c37d-414f-81fd-07f2d2d000d1">

### 해결
```javascript

```
