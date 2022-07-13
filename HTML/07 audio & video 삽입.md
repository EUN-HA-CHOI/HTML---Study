## 오디오와 비디오 삽입하기  
### 다양한 멀티미디어 파일을 삽입할 때 쓰는 object , embed 태그  

``` html
기본형 -> <object width="너비" height="높이" data="파일"></object>

기본형 -> <embed src="파일 경로" width="너비" height="높이">   <!--<embed>태그는 닫는 태그가 없다.-->
```
* 예시
``` html
<body>
  <object width="200" height="200" data="medias/Spring.mp3"></object>
</body>
```


<img width="218" alt="스크린샷 2022-05-20 오후 5 31 57" src="https://user-images.githubusercontent.com/97012561/169488178-d4d76f6b-0d2d-47b2-83f0-edd87b6a893c.png">


*웹 브라우저에서 지원하는 멀티미디어 파일의 종류 => 비디오는 mp4 ,오디오 파일은 mp3 형식을 주로 사용함.  

### 오디오와 비디오 파일을 삽입하는 audio , video 태그  
``` html 
기본형 -> <audio src="오디오 파일 경로"></audio>
기본형 -> <video src="비디오 파일 경로"></video>

<body>
  <audio src="medias/Spring.mp3"></audio>
</body>

*방문자가 음악을 재생하거나 멈출 수 있도록 컨트롤 바를 나타내는 controls 속성을 사용.
 <audio src="오디오 파일 경로" controls></audio>

*오디오 & 비디오 자동 재생하기
<video src="비디오 파일 경로" autoplay loop></video>
```


* 방문자가 음악을 재생하거나 멈출 수 있도록 컨트롤 바를 나타내는 controls 속성을 사용.

<img width="309" alt="스크린샷 2022-05-20 오후 5 39 46" src="https://user-images.githubusercontent.com/97012561/169489553-cc0b1617-ecf8-4be9-85b1-596a8bf71b5b.png">


```html
<body>
  <!-- 
    HTML5에서는 <video> 태그로 동영상 삽입,
    속성: src, poster, preload, autoplay, loop, controls, width, height
    단, 모바일 기기에서는 자동실행 안됨.
    muted: 비디오를 재생할 때 소리는 끄고 화면만 재생, 오디오를 
    문서 배경으로 사용하거나 소리가 필요하지 않을 때 사용
    type에 비디오 타입을 작성.
   -->
  
  <video width="480" height="272" poster="video/poster.jpg" autoplay controls loop muted>
    <source src="video/spring.mp4" type="video/mp4" />
    <source src="video/spring.ogv" type="video/dgv" />
    <source src="video/spring.webm" type="video/webm" />
  </video>
  <hr/>
  
  <!-- 유투브 동영상 첨가 공유하기 -> 퍼가기 -> 복사 -->
  <iframe width="560" height="315" src="https://www.youtube.com/embed/YKvx-igUpYc?start=48" 
  title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media;
   gyroscope; picture-in-picture" allowfullscreen>
   </iframe>
</body>
```

<img width="480" alt="스크린샷 2022-07-13 오후 11 27 33" src="https://user-images.githubusercontent.com/97012561/178758279-f96da45f-5120-4e9c-b36e-0d95d3526255.png">



```html
<!-- audio -->
<audio autoplay controls loop>
  <source src="audio/old_melody.mp3" type="audio/mp3" />
  <source src="audio/old_melody.ogg" type="audio/ogg" />
  <source src="audio/old_melody.wav" type="audio/wav" /> 
</audio>
```
<img width="301" alt="스크린샷 2022-07-13 오후 11 32 00" src="https://user-images.githubusercontent.com/97012561/178759332-9d4b337b-9fbb-4de0-9d61-9e0eb0ed12a9.png">


