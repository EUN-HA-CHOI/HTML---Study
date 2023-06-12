## 문제 1 : 배열 두 배 만들기  

### 문제 설명
정수 배열 numbers가 매개변수로 주어집니다. numbers의 각 원소에 두배한 원소를 가진 배열을 return하도록 solution 함수를 완성해주세요.

### 제한사항
- -10,000 ≤ numbers의 원소 ≤ 10,000
- 1 ≤ numbers의 길이 ≤ 1,000

### 입출력 예
<img width="376" alt="스크린샷 2023-06-12 오전 11 44 51" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/b486daf2-5ab8-4a5b-b94a-cfbb263ce69e">

### 해결
```javascript
function solution(numbers) {
    var answer = [];
    for(let i=0; i<numbers.length; i++){
      answer.push(numbers[i]*2);
    }
    return answer;
}
```

<hr>

## 문제 2 : 나머지 구하기

### 문제 설명
정수 num1, num2가 매개변수로 주어질 때, num1를 num2로 나눈 나머지를 return 하도록 solution 함수를 완성해주세요.

### 제한사항
- 0 < num1 ≤ 100
- 0 < num2 ≤ 100

### 입출력 예
<img width="191" alt="스크린샷 2023-06-12 오전 11 52 05" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/cabe7472-f220-4900-b8e1-a789df926c62">


### 해결
```javascript
function solution(num1, num2) {
    var answer = 0;
    return answer = num1%num2;
}
```

<hr>

## 문제 3 : 중앙값 구하기

### 문제 설명
중앙값은 어떤 주어진 값들을 크기의 순서대로 정렬했을 때 가장 중앙에 위치하는 값을 의미합니다. 예를 들어 1, 2, 7, 10, 11의 중앙값은 7입니다. 정수 배열 array가 매개변수로 주어질 때, 중앙값을 return 하도록 solution 함수를 완성해보세요.

### 제한사항
- array의 길이는 홀수입니다.
- 0 < array의 길이 < 100
- -1,000 < array의 원소 < 1,000

### 입출력 예
<img width="182" alt="스크린샷 2023-06-12 오전 11 56 40" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/8c020493-70a5-4345-8c04-7f7786eea6ea">

### 해결 (첫 시도 : 테스트만 통과하고 틀림.)
```javascript 
function solution(array) {
    array.sort();
    var center = parseInt(array.length / 2);
    if(array.length % 2 == 1) {
    return array[center];
    }
}
```

### 해결 (두 번째 시도)
```javascript 
function solution(array) {
    let answer = array.sort(function(a,b){
        return a-b });  //오름차순 정렬 answer에 할당
    var center = parseInt(array.length / 2);  // 배열의 길이를 2로 나눈 몫을 할당
    if(array.length % 2 == 1) {  // 나눈 값이 홀수인 경우 
    return answer = array[center];
    }
}
//여기서 더 수정 할 수도 있을 것 같음.
```

<hr>

## 문제 4 : 최빈값 구하기

### 문제 설명
최빈값은 주어진 값 중에서 가장 자주 나오는 값을 의미합니다. 정수 배열 array가 매개변수로 주어질 때, 최빈값을 return 하도록 solution 함수를 완성해보세요. 최빈값이 여러 개면 -1을 return 합니다.

### 제한사항
- 0 < array의 길이 < 100
- 0 ≤ array의 원소 < 1000

### 입출력 예
<img width="185" alt="스크린샷 2023-06-12 오후 2 02 48" src="https://github.com/EUN-HA-CHOI/HTML-CSS-JS-Study/assets/97012561/070277c7-4a54-45d9-ac8b-64894b31aef8">

### 해결 (x)
```javascript
function solution(array) {
  // array의 길이가 1일 경우 갯수가 하나이기에
  // 그 값을 반환해준다.
  if (array.length === 1) return array[0];

  const obj = {};
  const answer = [];

  // array를 forEach() 반복문을 돌려
  // obj에 값이 없으면 값을 만들고 1을 넣어주고
  // obj에 값이 있으면 기존 값 +1을 해준다.
  array.forEach((n) => {
    obj[n] = ++obj[n] || 1;
  });

  // 값과 그 값의 갯수를 정의해 둔 obj를 array에 넣어준다.
  // ex) [[1, 1], [2, 1], [3, 3], [4, 1]]
  for (let key in obj) {
    answer.push([key, obj[key]]);
  }

  // answer 배열을 갯수 기준으로 내림차순 정렬을 해준다.
  // ex) [[3, 3], [4, 1], [2, 1], [1, 1]]
  answer.sort((a, b) => b[1] - a[1]);

  // 최빈값이 여러 개면 -1을 반환해야 하기 때문에 확인한다.
  if (answer.length > 1 && answer[0][1] === answer[1][1]) return -1;

  // 여러개가 아니라면 정렬한 처음 값을 반환한다.
  return Number(answer[0][0]);
}
```
