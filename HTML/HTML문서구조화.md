# HTML 문서 구조화
## 인라인 / 블록 요소
- HTML 요소는 크게 인라인 / 블록 요소로 나눔
- 인라인 요소는 글자처럼 취급
- 블록 요소는 한 줄 모두 사용

## 텍스트 요소
- <a></a>   :   href 속성을 활용하여 다른 URL로 연결하는 하이퍼링크 생성
- <b></b>   :   굵은 글씨 요소
- <strong></strong> :  중요한 강조하고자 하는 요소 (보통 굵은 글씨로 표현)
- <i></i>   :   기울임 글씨 요소
- <em></em> :   중요한 강조하고자 하는 요소 (보통 기울임 글씨로 표현)
- <br>  :   텍스트 내에 줄 바꿈 생성
- <img> :   src 속성을 활용하여 이미지 표현
- <span></span> : 의미 없는 인라인 컨테이너

## 그룹 컨텐츠
- <p></p>   :   하나의 문단(paragraph)
- <hr>  :  문단 레벨 요소에서의 주제의 분리를 의미하며 수평선으로 표현됨 (A Horizontal Rule)
- <ol></ol> : 순서가 있는 리스트(ordered)
- <ul></ul> : 순서가 없는 리스트(unordered)
- <pre></pre>   :   HTML에 작성한 내용을 그대로 표현, 보통 고정폭 글꼴이 사용되고 공백 문자를 유지
- <blockquote></blockquote> : 텍스트가 긴 인용문, 주로 들여쓰기를 한 것으로 표현됨
- <div></div>   :   의미 없는 블록 레벨 컨테이너

## form
- <form>은 정보(데이터)를 서버에 제출하기 위해 사용하는 태그
- <form> 기본 속성
    - action : form을 처리할 서버의 URL(데이터를 보낼 곳)
    - method : form을 제출할 때 사용할 HTTP 메서드 (GET 혹은 POST)
    - enctype : method가 post인 경우 데이터의 유형
        - application/x-www-form-urlencoded : 기본값
        - multipart/form-data : 파일 전송시 (input type이 file인 경우)
        - text/plain : HTML5 디버깅 용 (잘 사용되지 앟음)
```
<form action="/search" method="GET">

</form>
```

## input
- 다양한 타입을 가지는 입력 데이터의 유형과 위젯이 제공됨
- <input> 대표적인 속성
    - name : form control에 적용되는 이름 (이름/값 페어로 전송됨)
    - value : form control에 적용되는 값 (이름/값 페어로 전송됨)
    - required, readonly, autofocus, autocomplete, disabled 등
```
<form action="/search" method="GET">
  <input type="text" name="q">
</form>
```

## input label
- label을 클릭하여 input 자체의 초점을 맞추거나 활성화 시킬 수 있음
    - 사용자는 선택할 수 있는 영역이 늘어나 웹 / 모바일(터치) 환경에서 편하게 사용할 수 있음
    - label과 input 입력의 관계가 시각적 뿐만 아니라 화면 리더기에서도 label을 읽어 쉽게 내용을 확인할 수 있도록 함
- <input>에 id 속성을, <label>에는 for 속성을 확용하여 상호 연관을 시킴
```
<label for="agreement">개인정보 수집에 동의합니다.</label>
<input type="checkbox" name="agreement" id="agreement">
```

## input 유형 - 일반
- 일반적으로 입력을 받기 위하여 제공되며 타입별로 HTML 기본 검증 혹은 추가 속성을 활용할 수 있음
    - text : 일반 텍스트 입력
    - password : 입력 시 값이 보이지 않고 문자를 특수기호(*)로 표현
    - email : 이메일 형식이 아닌 경우 form 제출 불가
    - number : min, max, step 속성을 활용하여 숫자 범위 설정 가능
    - file : accept 속성을 활용하여 파일 타입 지정 가능

## input 유형 - 항목 중 선택
- 일반적으로 label 태그와 함께 사용하여 선택 항목을 작성함
- 동일 항목에 대하여는 name을 지정하고 선택된 항목에 대한 value를 지정해야 함
    - checkbox : 다중 선택
    - radio : 단일 선택

## input 유형 - 기타
- 다양한 종류의 input을 위한 picker를 제공
 - color : color picker
 - date : date picker
- hidden input을 활용하여 사용자 입력을 받지 않고 서버에 전송되어야 하는 값을 설정
    - hidden : 사용자에게 보이지 않는 input

## input 유형 - 종합
- <input> 요소의 동작은 type에 따라 달라지므로, 각각의 내용을 숙지할 것

## 마크업 해보기
- 구조
    - 1. header
    - 2. section
    - 3. footer