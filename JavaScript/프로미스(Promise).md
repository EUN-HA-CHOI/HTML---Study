## 프로미스(Promise)란?  

프로미스는 비동기 처리를 위한 또다른 방법. (콜백함수의 단점을 보완하며 비동기 처리 시점을 명확하게 표현할 수 있는 장점이 있음.)   

* 프로미스의 장점  
  * 비동기 처리 시점을 명확하게 표현할 수 있다.  
  * 연속된 비동기 처리 작업을 수정, 삭제, 추가하기 편하고 유연하다.  
  * 비동기 작업 상태를 쉽게 확인할 수 있다.  
  * 코드의 유지 보수성이 증가한다.    
  
프로미스는 객체이기에 생성자 함수를 호출하여 인스턴스화  (인스턴스화: 데이터 필드의 저장 유형 및 값과 같은 정보를 읽거나 지정하는 프로세스)  
프로미스의 생성자 함수는 resovle와 reject 함수를 인자로 전달받는 콜백함수를 인자로 전달 받는다.   
프로미스는 인자로 전달받은 콜백함수를 내부에서 비동기 처리한다.  

프로미스는 비동기 처리가 성공(fulfilled) or 실패(rejected) 등의 상태 정보를 갖게 된다.    
resovle 함수가 호출 된 경우 성공 , reject 함수가 호출 된 경우 실패.  

```
const promise = () => new Promise((resolve, reject) => {
    let a = 1 + 1

    if(a == 2) {
        resolve('success')
    } else {
        reject('failed')
    }
})

promise().then((message) => {
    console.log('This is in the then ' + message)
}).catch((message) => {
    console.log('This is in the catch' + message)
})
```
promise 라는 이름의 전역 변수에 프로미스를 할당 하였고 그 안에는 1 + 1 이 2라면 resolve 함수를 호출하고 아니면 reject 함수를 호출하도록 구현했다.  
그 다음 프로미스의 후속 처리 메소드인 then(), catch()를 통해 비동기 처리 결과 메세지를 전달받아 처리하였다.   

* **후속 처리 메소드**  
프로미스로 구현된 비동기 함수를 호출하는 측에서는 프로미스 객체의 후속 처리 메소드(then, catch)를 통해 비동기 처리 결과 또는 에러 메세지를 전달받아 처리한다.  

* then
   * then 메소드는 두 개의 콜백 함수를 인자로 전달 받습니다.  
   * 첫 번째 콜백 함수는 성공(fulfilled, resolve 함수가 호출된 경우)시에 실행됩니다.  
   * 두 번째 콜백 함수는 실패(rejected, reject 함수가 호출된 경우)시에 실행됩니다.  
   * then 메소드는 기본적으로 프로미스를 반환합니다.  
   
* catch    
   * catch 메소드는 비동기 처리 혹은 then 메소드 실행 중 발생한 에러(예외)가 발생하면 호출됩니다.  
   * catch 메소드 역시 프로미스를 반환합니다.  
   
**프로미스 에러 처리 방법**  
프로미스 에러 처리는 가급적 catch 메소드를 이용하는 것이 좋다. 그 이유는 다음과 같다.  

 resolve 함수가 정상적으로 호출되고 프로미스가 성공 상태가 되며 then 메소드의 첫 번째 콜백함수가 실행된다.   
첫 번째 콜백함수에서 에러가 발생하였고 두 번째 콜백함수가 에러를 잡아내지 못하고 있다.   
```
const promise = () => new Promise((resolve, reject) => {
    let a = 1 + 1

    if(a == 2) {
        resolve('success')
    } else {
        reject('failed')
    }
})

promise().then((message) => {
    console.log('This is in the then ' +  message)
    throw new Error('failed')
}, (error) => {
    console.log('This is in the then ' + error)
})
```
```
This is in the then success
(node:52580) UnhandledPromiseRejectionWarning: Error: failed
```

catch 메소드를 사용하는 경우에는 then 메소드의 첫 번째 콜백함수에서 발생하는 에러를 잡아내는 것을 볼 수 다.

```
const promise = () => new Promise((resolve, reject) => {
    let a = 1 + 1

    if(a == 2) {
        resolve('success')
    } else {
        reject('failed')
    }
})

promise().then((message) => {
    console.log('This is in the then ' +  message)
    throw new Error('failed')
}).catch((error) => {
    console.log('This is in the catch ' +  error)
})
```
```
This is in the then success
This is in the catch Error: failed
```


  

