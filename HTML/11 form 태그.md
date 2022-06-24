## 폼에서 사용하는 여러 가지 태그
### 여러 줄을 입력하는 텍스트 영역 textarea 태그
```html
기본형 -> <textarea>내용</textarea>
```
### 드롭 다운 목록을 만들어 주는 select , option 태그
``` html
기본형 -> <select>
           <option value="값1">내용1</option>
           <option value="값2">내용2</option>
        </select>
```

### 데이터 목록 만들어 주는 datalist , option 태그
*데이터 목록을 사용하면 텍스트 필드에 값을 직접 입력하지 않고 미리 만들어 놓은 값 중에서 선택 가능.
``` html
기본형 -> <input type="text" list="데이터 목록 id">
        <datalist id="데이터 목록 id">
           <option value="서버로 넘길 값1">선택 옵션1</option>
           <option value="서버로 넘길 값2">선택 옵션2</option>
       </datalist>
```

### 버튼을 만들어주는 button 태그
*button 태그를 이용하여 폼을 전송하거나 리셋하는 버튼을 삽입할 수 있다.
```html 
기본형 -> <button type="submit">내용</button>
        <button type="reset">내용</button>
        <button type="button">내용</button>

         
