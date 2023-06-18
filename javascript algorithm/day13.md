## 문제 1 : 중복된 숫자 개수

### 문제 설명
정수가 담긴 배열 array와 정수 n이 매개변수로 주어질 때, array에 n이 몇 개 있는 지를 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 1 ≤ array의 길이 ≤ 100
- 0 ≤ array의 원소 ≤ 1,000
- 0 ≤ n ≤ 1,000

### 입출력 예 
<img width="254" alt="스크린샷 2023-06-18 오후 3 29 40" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/e6de5b54-87af-4482-8f87-e55b98d905fd">

### 해결 
```javascript
function solution(array, n) {
    var answer = 0;
    for(let i=0; i<array.length; i++){
        if(array[i] === n) {
            answer++;
     }
    }
    return answer;
}
```

<hr>

## 문제 2 : 문자열이 몇 번 등장하는지 세기

### 문제 설명
문자열 myString과 pat이 주어집니다. myString에서 pat이 등장하는 횟수를 return 하는 solution 함수를 완성해 주세요.

### 제한사항
- 1 ≤ myString ≤ 1000
- 1 ≤ pat ≤ 10

### 입출력 예 
<img width="217" alt="스크린샷 2023-06-18 오후 3 43 23" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/0126db5d-b979-41d3-818c-5ee1051733f9">

### 해결 (x)
```javascript
function solution(myString,pat) {
    return [...myString].reduce((acc, cur, idx) => {
        const curStr = myString.slice(idx, pat.length+idx)
        if(curStr === pat) return acc+1;
        return acc;
    }, 0)
}
```

<hr>

## 문제 3 : 다음에 올 숫자

### 문제 설명
등차수열 혹은 등비수열 common이 매개변수로 주어질 때, 마지막 원소 다음으로 올 숫자를 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 2 < common의 길이 < 1,000
- 1,000 < common의 원소 < 2,000
  - common의 원소는 모두 정수입니다.
- 등차수열 혹은 등비수열이 아닌 경우는 없습니다.
- 등비수열인 경우 공비는 0이 아닌 정수입니다.

### 입출력 예 
<img width="157" alt="스크린샷 2023-06-18 오후 5 10 22" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/58e9426b-a136-4749-9905-fc896c036ef0">


### 해결
```javascript

```
