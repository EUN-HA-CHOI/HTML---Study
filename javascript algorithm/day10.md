## 문제 1 : 배열 뒤집기 

### 문제 설명
정수가 들어 있는 배열 num_list가 매개변수로 주어집니다. num_list의 원소의 순서를 거꾸로 뒤집은 배열을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- 1 ≤ num_list의 길이 ≤ 1,000
- 0 ≤ num_list의 원소 ≤ 1,000

### 입출력 예 
<img width="278" alt="스크린샷 2023-06-14 오후 12 58 31" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/072f0bca-6336-45cd-b3cb-190badf046bb">


### 해결 
```javascript
function solution(num_list) {
    let reverse = num_list.reverse();
    return reverse;
}
```

<hr>

## 문제 2 : 직각삼각형 출력하기 

### 문제 설명
"*"의 높이와 너비를 1이라고 했을 때, "*"을 이용해 직각 이등변 삼각형을 그리려고합니다. 정수 n 이 주어지면 높이와 너비가 n 인 직각 이등변 삼각형을 출력하도록 코드를 작성해보세요.

### 제한사항
- 1 ≤ n ≤ 10

### 입출력 예 
<img width="212" alt="스크린샷 2023-06-14 오후 12 59 41" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/34582bf9-f581-4a78-9ff2-7c9886328144">


### 해결 (테스트는 통과인데 답을 틀려서 수정해야됨)
```javascript
let linecount = 3;
let star = "";

for(i = 0; i < linecount; i++) {
	for(j = 0; j <= i; j++) {
      star += "*";
    }
  	star += '\n';
}
console.log(star);
```

<img width="230" alt="스크린샷 2023-06-14 오후 1 00 06" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/3cc27b11-34d3-486c-85ff-a69bdcdf948d">


<hr>


## 문제 3 : 짝수 홀수 개수

### 문제 설명
정수가 담긴 리스트 num_list가 주어질 때, num_list의 원소 중 짝수와 홀수의 개수를 담은 배열을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- 1 ≤ num_list의 길이 ≤ 100
- 0 ≤ num_list의 원소 ≤ 1,000

### 입출력 예 
<img width="174" alt="스크린샷 2023-06-14 오후 1 01 12" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/4b819075-c692-45fb-9869-8f3036668c79">


### 해결 (세모)
```javascript
function solution(num_list) {
    var answer = [0,0];
    for(let x of num_list) {
        answer[x%2]++;
    }
    return answer;
}
```
- 짝수 홀수 찾는 방법은 숫자%2 해서 나머지 값으로 알아낸다. 1이면 홀수, 0이면 짝수.  
- for 문으로 배열의 요소를 순회하여 짝수,홀수 찾는다. 
- 홀수,짝수 찾아냄과 동시에 그 값을 answer 의 인덱스 번호로 넣는다. 
- 홀수라면 값은 1이 나온다. 1을 answer의 인덱스에 넣고 값을 증가시키면 1번 인덱스에 자동으로 홀수의 값이 쌓이게 된다. 



<hr>
