## 오디오와 비디오 삽입하기  
### 다양한 멀티미디어 파일을 삽입할 때 쓰는 object , embed 태그  
``` html
기본형 -> <object width="너비" height="높이" data="파일"></object>

기본형 -> <embed src="파일 경로" width="너비" height="높이">   <!--<embed>태그는 닫는 태그가 없다.-->
```

*웹 브라우저에서 지원하는 멀티미디어 파일의 종류 => 비디오는 mp4 ,오디오 파일은 mp3 형식을 주로 사용함.  

### 오디오와 비디오 파일을 삽입하는 audio , video 태그  
``` html 
기본형 -> <audio src="오디오 파일 경로"></audio>
기본형 -> <video src="비디오 파일 경로"></video>

*방문자가 음악을 재생하거나 멈출 수 있도록 컨트롤 바를 나타내는 controls 속성을 사용.
 <audio src="오디오 파일 경로" controls></audio>

*오디오 & 비디오 자동 재생하기
<video src="비디오 파일 경로" autoplay loop></video>
```







