## 문제 1 : 모음 제거

### 문제 설명
영어에선 a, e, i, o, u 다섯 가지 알파벳을 모음으로 분류합니다. 문자열 my_string이 매개변수로 주어질 때 모음을 제거한 문자열을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- my_string은 소문자와 공백으로 이루어져 있습니다.
- 1 ≤ my_string의 길이 ≤ 1,000

### 입출력 예
<img width="247" alt="스크린샷 2023-06-16 오후 1 36 05" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/1d50487c-a7d3-431c-a345-272d1d711bba">

### 입출력 예 설명
- "bus"에서 모음 u를 제거한 "bs"를 return합니다.
- "nice to meet you"에서 모음 i, o, e, u를 모두 제거한 "nc t mt y"를 return합니다.

### 해결 (x)
```javascript
function solution(my_string) {
    let a = ['a','e','i','o','u']
    for(let i = 0; i<a.length;i++){
       my_string = my_string.replaceAll(a[i],'')
    }
    return my_string
}
```

<hr>

## 문제 2 : 배열 원소의 길이

### 문제 설명
문자열 배열 strlist가 매개변수로 주어집니다. strlist 각 원소의 길이를 담은 배열을 retrun하도록 solution 함수를 완성해주세요.

### 제한사항
- 1 ≤ strlist 원소의 길이 ≤ 100
- strlist는 알파벳 소문자, 대문자, 특수문자로 구성되어 있습니다.

### 입출력 예
<img width="324" alt="스크린샷 2023-06-16 오후 1 37 55" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/1728d026-9e4e-4d6e-a1ba-a2a18797bd96">

### 입출력 예 설명
- ["We", "are", "the", "world!"]의 각 원소의 길이인 [2, 3, 3, 6]을 return합니다.
- ["I", "Love", "Programmers."]의 각 원소의 길이인 [1, 4, 12]을 return합니다.

### 해결
```javascript
function solution(strlist) {
    var answer = [];
    for(let i=0; i<strlist.length; i++){
      answer.push(strlist[i].length);
    }
    return answer;
}
```
