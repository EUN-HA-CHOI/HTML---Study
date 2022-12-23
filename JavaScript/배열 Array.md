## 배열 Array  

배열은 이름과 인덱스로 참조되는 정렬된 값의 집합으로 정의 된다.    
배열을 구성하는 각각의 값을 배열 요소(element)라고 하며, 배열에서의 위치를 가리키는 숫자를 인덱스(index)라고 한다.  

* 특징  
  * 배열 요소의 타입이 고정되어 있지 않으므로, 같은 배열에 있는 배열 요소끼리의 타입이 서로 다를 수 있다.  
  * 배열 요소의 인덱스가 연속적이지 않아도 되며, 특정 배열 요소가 비어 있을 수도 있다.   
  * javascript 에서 배열은 Array 객체로 다뤄진다.   


* 배열 생성   
```
1. var arr = [배열요소1, 배열요소2,...];          // 배열 리터럴을 이용하는 방법

2. var arr = Array(배열요소1, 배열요소2,...);     // Array 객체의 생성자를 이용하는 방법

3. var arr = new Array(배열요소1, 배열요소2,...); // new 연산자를 이용한 Array 객체 생성 방법
```

위의 세 가지 방법 모두 같은 결과의 배열을 만든다. 배열 리터럴은 대괄호([]) 안에 배열 요소를 쉼표로 구분하여 나열하는 방법으로 생성한다.   

* 배열의 참조  
  자바스크립트에서 배열의 각 요소를 참조하고 싶을 때는 [] 연산자를 사용한다.  
  배열이름[인덱스]  
  
  자바스크립트에서는 배열 요소의 개수를 배열의 길이라고 한다.  
  이러한 배열의 길이는 length 프로퍼티에 자동으로 갱신된다.  
  
  자바스크립트에서 인덱스는 언제나 0부터 시작    
  인덱스에서는 음이 아닌 정수를 반환하는 임의의 표현식도 사용할 수 있다.  
  이러한 인덱스에는 2의 23승 보다 작은 양수만을 사용할 수 있다.   
  
* 예제 
```
var arr = ["JavaScript"]; // 요소가 하나뿐인 배열을 생성함.
var element = arr[0];     // 배열의 첫 번째 요소를 읽어서 대입함.

arr[1] = 10;      // 배열의 두 번째 요소에 숫자 10을 대입함. 배열의 길이는 1에서 2로 늘어남.
arr[2] = element; // 배열의 세 번째 요소에 변수 element의 값을 대입함. 배열의 길이는 2에서 3으로 늘어남.

document.write("배열 arr의 요소에는 [" + arr + "]가 있습니다.<br>"); // 배열의 요소를 모두 출력함.
document.write("배열 arr의 길이는 " + arr.length + "입니다.<br>");   // 배열의 길이를 출력함.

delete arr[2];    // 배열의 세 번째 요소를 삭제함. 하지만 배열의 길이는 변하지 않음.

document.write("배열 arr의 요소에는 [" + arr + "]가 있습니다.<br>"); // 배열의 요소를 모두 출력함.
document.write("배열 arr의 길이는 " + arr.length + "입니다.");       // 배열의 길이를 출력함.
```

배열의 현재 길이보다 더 큰 인덱스에 요소를 저장하려고 한다. 자바스크립트에서는 배열의 길이를 넘는 인덱스에 요소를 저장하는 것을 허용한다.  
이때 배열의 길이는 자동으로 해당 인덱스까지 늘어난다.   


* 배열 요소의 추가  
  * arr.push(추가할 요소);         // push() 메소드를 이용하는 방법     
  * arr[arr.length] = 추가할 요소; // length 프로퍼티를 이용하는 방법   
  * arr[특정인덱스] = 추가할 요소; // 특정 인덱스를 지정하여 추가하는 방법      
 
push() 메소드와 length 프로퍼티를 이용한 방법은 모두 배열의 제일 끝에 새로운 요소를 추가.  

* 예제  
```
var arr = [1, true, "Java"];
arr.push("Script");           // push() 메소드를 이용하는 방법
document.write(arr + "<br>"); // 1,true,Java,Script

arr[arr.length] = 100;        // length 프로퍼티를 이용하는 방법
document.write(arr + "<br>"); // 1,true,Java,Script,100

arr[10] = "자바스크립트";     // 특정 인덱스를 지정하여 추가하는 방법
document.write(arr + "<br>"); // 1,true,Java,Script,100,,,,,,자바스크립트
document.write(arr[7]);       // undefined
```

배열 arr의 길이는 11이다. 이때 배열 요소가 존재하는 인덱스는 0, 1, 2, 3, 4, 10뿐이며, 나머지 인덱스에는 배열 요소가 존재하지 않는다.    

이렇게 인덱스에 대응하는 배열 요소가 없는 부분을 배열의 홀(hole)이라고 한다. 자바스크립트에서는 이러한 배열의 홀(hole)을 undefined 값을 가지는 요소처럼 취급합니다.   
따라서 위의 예제에서처럼 배열의 홀을 참조하게 되면 undefined 값을 반환하게 됩니다.   
 

## ForEach 메서드란 ?  

forEach() 메서드는 배열에 활용이 가능한 메서드로, 파라미터로 주어진 함수를 배열 요소 각각에 대해 실행하는 메서드이다.  
map() 메서드와 거의 비슷하지만 차이점은 따로 return 하는 값이 없다는 점이다.   

```
const myArr = [1, 2, 3, 4, 5];

const newMyArr = myArr.forEach((currentElement, index, array) => {
    console.log(`요소: ${currentElement}`);
    console.log(`index: ${index}`);
    console.log(array);
});

console.log(newMyArr); // undefined
```

forEach 메서드도 map메서드와 동일하게 파라미터로 콜백 함수를 받는데, 그 콜백 함수의 파라미터는 요소, index 그리고 현재 map메서드를 호출한 배열이다.       
forEach 메서드도 세번째 배열은 잘 사용되지 않고 일반적으로 첫 번째 요소와, 두 번째 index가 많이 사용된다.      

map 메서드와 차이점은 따로 콜백 함수가 return 하는 값을 따로 모아서 어떤 처리를 하는 과정이 없기 때문에, 메서드를 호출한 코드를 함수에 할당하면 undefined가 할당된다.     
그래서 forEach 메서드는 변수에 할당하기 보다는 반복문이나 조건문과 같이 그냥 바로 호출되는 것이 일반적이다.     

```
const myArr = [1, 2, 3, 4, 5];

myArr.forEach((currentElement, index, array) => {
    console.log(`요소: ${currentElement}`);
    console.log(`index: ${index}`);
    console.log(array);
});
```

## map() 매서드란 ?  

배열(arr)의 각각의 element들이 callback 함수의 파라미터로 전달되고, map() 함수는 이 callback 함수가 return 하는 값으로 새로운 배열을 만들어서 리턴한다.      
 
* 파라미터    
  * currentValue : 현재 처리중인 배열의 element   
  * index(optional) : 현재 처리중인 배열의 index    
  * array(optional) : 현재 처리중인 배열     

* callback함수에 의해서 변경된 arr의 새로운 배열이 리턴된다. 이때, 원래의 배열인 arr는 변경되지 않는다.     

* 예제 

```
const arr1 = [1, 2, 3, 4];

const arr2 = arr1.map((currValue) => currValue + 1);
const arr3 = arr1.map(function add(currValue) {
  return currValue + 1;
})

document.writeln(arr1 + '<br>'); // [1, 2, 3, 4]
document.writeln(arr2 + '<br>'); // [2, 3, 4, 5]
document.writeln(arr3 + '<br>'); // [2, 3, 4, 5]

result 
1,2,3,4
2,3,4,5
2,3,4,5
```

map() 함수를 사용하여 배열의 모든 값에 1을 더한 새로운 배열을 생성했다.    

* 예제1
```
const arr1 = [1, 2, 3, 4];

const arr2 = arr1.map(function add(currValue) {
  currValue = currValue + 1;
})

document.writeln(arr1 + '<br>'); // [1, 2, 3, 4]
document.writeln(arr2[0] + '<br>'); // undefined

result 
1,2,3,4
undefined
```

map() 함수의 callback 함수는, 반드시 새로운 배열의 element가 될 값을 리턴해 주어야 한다.    

위와 같이 실수하지 않도록 주의해야 한다. callback 함수에서 값을 리턴하지 않으면, map() 함수에 의해 생성되는 새로운 배열(arr2)의 element는 undefined 값을 가지게 되고,    
arr1의 값도 변경되지 않습니다.   

