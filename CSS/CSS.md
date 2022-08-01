# CSS
## CSS (Cascading Style Sheets)
### 스타일을 지정하기 위한 언어 / 선택하고, 스타일을 지정한다.
```
h1 {
    color: blue;
    font-size: 15px;
}
# h1 -> 선택자(Selector)
# color: blue -> 선언(Declaration)
# font-size -> 속성(Property)
# 15px -> 값(Value)
```
- CSS 구문은 선택자를 통해 스타일을 지정할 HTML 요소를 선택
- 중괄호 안에서는 속성과 값, 하나의 쌍으로 이루어진 선언을 진행
- 각 쌍은 선택한 요소의 속성, 속성에 부여할 값을 의미
    - 속성 (Property) : 어떤 스타일 기능을 변경할지 결정
    - 값 (Value) : 어떻게 스타일 기능을 변경하지 결정

## CSS 정의 방법
- 인라인(inline)
    - 해당 태그에 직접 style 속성을 활용
- 내부 참조(embedding) - <style>
    - <head> 태그 내에 <style>에 지정
- 외부 참조(link file) - 분리된 CSS 파일
    - 외부 CSS 파일을 <head>내 <link>를 통해 불러오기

- 1. 인라인(lnline)
    - 인라인을 쓰게 되면 실수가 잦아짐(중복도 있을 것이고, 찾기가 어려워서)
- 2. 내부 참조(embedding) - <style>
    - 내부 참조를 쓰게 되면 코드가 너무 길어짐
- 3. 외부 참조(link file) - 분리된 CSS 파일
    - 가장 많이 쓰는 방식

## CSS with 개발자 도구
- styles : 해당 요소에 선언된 모든 CSS
- computed : 해당 요소에 최종 계산된 CSS

# CSS Selectors
```
h1 {
    color: blue;
    font-size: 15px;
}
# h1 -> 선택자(Selector)
# color: blue -> 선언(Declaration)
# font-size -> 속성(Property)
# 15px -> 값(Value)
```

## 선택자(Selector) 유형
- 기본 선택자
    - 전체 선택자, 요소 선택자
    - 클래스 선택자, 아이디 선택자, 속성 선택자
- 결합자(Combinators)
    - 자손 결합자, 자식 결합자
    - 일반 형제 결합자, 인접 형제 결합자
- 의사 클래스/요소(Pseudo Class)
    - 링크, 동적 의사 클래스
    - 구조적 의사 클래스, 기타 의사 클래스, 의사 엘리먼트, 속성 선택자

## CSS 선택자 정리
- 요소 선택자
    - HTML 태그를 직접 선택
- 클래스(class) 선택자
    - 마침포(.) 문자로 시작하며, 해당 클래스가 적용된 항목을 선택
- 아이디(id) 선택자
    - #문자로 시작하며, 해당 아이디가 적용된 항목을 선택
    - 일반적으로 하나의 문서에 1번만 사용
    - 여러 번 사용해도 동작하지만, 단일 id를 사용하는 것을 권장

## CSS 적용 우선순위(Cascading Order)
- CSS 우선순위를 아래와 같이 그룹을 지어볼 수 있다,
    - 1. 중요도(Importance) - 사용시 주의
        - !important
    - 2. 우선 순위(Specificity)
        - 인라인 > id > class, 속성, pseudo-class > 요소, pseudo-element
    - 3. CSS 파일 로딩 순서

## CSS 상속
- CSS는 상속을 통해 부모 요소의 속성을 자식에게 상속된다.
    - 속성(프로퍼티) 중에는 사용이 되는 것과 되지 않는 것들이 있다.
    - 상속 되는 것 예시
      예) Text 관련 요소(font, color, text_align, bisibility) 등
    - 상속 되지 않는 것 예시
      예) Box model 관련 요소(width, height, margin, padding, box-sizing, display), position 관련 요소(position, top/right/bottom/left/z-index)등)

## css 상속 - MDN에서 확인하기
```
<body>
  <p>안녕하세요! <span>테스트</span> 입니다. </p>
  </body>
```
```
<styile>
  p {}
    /* 상속됨 */
    color:rea;
    /* 상속 안됨*/
    border: 3px solid black:
  }
  span (
  )
  </style>
  ```