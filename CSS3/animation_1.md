### css3 : animation  

```css
<style>
  body {
    margin: 0;
    padding: 0;
    background: url(ruler.jpg) no-repeat 0 0;
  }
  div {
    position: relative;
    width: 100px;
    height: 100px;
    border-radius: 50px;
    border: 2px solid black;
    background: url(f1.png) no-repeat 0 0;
    animation: ani 10s linear 0s infinite alternate;
  }
  @keyframes ani {
    0% {
      left: 0;
      border: 20px solid red;
    }
    50% {
      top: 50px;
      border: 20px solid blue;
    }
    100% {
      left: 1000px;
      border: 20px solid yellow;
      background-image: url(f2.png);
    }
  }
  /*
  animation: 모션이름 시간 가속도 delay 반복횟수 방향지정;
  @keyframes 모션이름 {
    0%{모션 시작점의 css 설정}
    100% {모션 끝점의 css설정}
  }
  0%, 100% 대신 from,to 사용가능
  
  animation-name : 모션이름
  animation-duration : 0%~100% 까지의 실행속도를 초단위로 설정, 1s , 100ms
  animation-timing-function 가속도: linear 가속도 없음, ease 가속도 있음
  animation-delay : 대기시간
  animation-interction-count 반복횟수: 0~100% 까지의 반복회수 지정, infinite 무한반복
  animation-direction 방향: normal (0~`00% 반복실행),alternate(0~100%완료시 다시 100~0% 반복), reverse
  animation-fill-mode: 애니메이션이 시작되기 전이나 끝나고 난 후 효과 forwards, backwards,both,none
  animation-play-state: 애니메이션의 실행 상태를 설정, paused
  animation-steps() : steps(10) 애니메이션 동작 지정
  */
</style>
```
[적용 결과](http://127.0.0.1:5500/animation.html)
