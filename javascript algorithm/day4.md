## 문제 1 : 마지막 두 원소  

### 문제 설명
정수 리스트 num_list가 주어질 때, 마지막 원소가 그전 원소보다 크면 마지막 원소에서 그전 원소를 뺀 값을 마지막 원소가 그전 원소보다 크지 않다면 마지막 원소를 두 배한 값을 추가하여 return하도록 solution 함수를 완성해주세요.

### 제한사항
2 ≤ num_list의 길이 ≤ 10
1 ≤ num_list의 원소 ≤ 9

### 입출력 예  
<img width="244" alt="스크린샷 2023-06-02 오후 2 31 51" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/15d2c28f-2f39-4021-a283-222a2f156483">


### 해결 (x)
```javascript
function solution(num_list) {
    var answer = [];
    return num_list.at(-2) >= num_list.at(-1) ? [...num_list, num_list.at(-1)*2] : [...num_list, num_list.at(-1)-num_list.at(-2)]
}
```

<hr>

## 문제 2 : 수 조작하기  

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

### 입출력 에  
<img width="271" alt="스크린샷 2023-06-02 오후 3 28 51" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/0bb7e513-6af0-49e3-b706-3aa6d281b740">

### 해결 
```javascript

```
