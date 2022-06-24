## 사용자 입력을 위한 input 태그  
### 웹 폼의 다양한 곳에서 사용하는 input 태그
*input 태그는 다양한 폼에서 사용자가 입력한 정보를 받을 때 사용.  

### input 태그의 type 속성. 
  
### 텍스트와 비밀번호를 나타내는 type="text" 와 type="password". 
```html
기본형 -> <input type="text">
        <input type="password">
```

### 체크박스와 라디오 버튼을 나타내는 type="checkbox" , type="radio"
```html
기본형 -> <input type="checkbox">
        <input type="radio">
```

### 숫자 입력 필드를 나타내는 type="number" , type="range". 
```html
기본형 -> <input type="numbe">
        <input type="range">
```

### 날짜 입력을 나타내는  type="date" , type="month" , type="week" 
```html
기본형 -> <input type="date | month | week"> 
 
 type="date"  "yyyy-mm-dd"로 표시됨
 type="month" "yyyy-mm"로 표시됨
 type="week"  1월 첫째 주 기준으로 몇 번째 주인지 표시됨
```

### 시간 입력을 나타내는 type="time" ,  type="datetime" ,  type="datetime-local"
```html
기본형 -> <input type="time | datetime | datetime-local"> 

 type="time"  3개의 항목으로 나타나며 첫 번째 항목부터 '오전' 과 '오후' 나머지는 '시' 와 '분'
 type="datetime" ,  type="datetime-local" 사용자가 웹 문서를 보고 있는 지역에 맞는 날짜와 시간을 함께 입력할 수 있다.
```

### 전송 , 리셋 버튼을 나타내는 type="submit" , type="reset". 
```html
기본형 -> <input type="submit | reset" value="버튼에 표시할 내용">
```

### 이미지 버튼을 나타내는 type="image" 
```html
기본형 -> <input type="image" src="이미지 경로" alt="대체 텍스트">
```

### 기본 버튼을 나타내는 type="button"
```html
기본형 -> <input type="button value="버튼에 표시할 내용">
```

### 파일을 첨부할 때 사용하는 type="file"
```html
기본형 -> <input type="file">
```

### 히든 필드 만들 때 사용하는 type="hidden">
*화면의 폼에는 보이지 않지만 사용자가 입력을 마치면 폼과 함께 서버로 전송되는 요소 
```html
기본형 -> <input type="hidden" name="이름" value="서버로 넘길 값">
```


