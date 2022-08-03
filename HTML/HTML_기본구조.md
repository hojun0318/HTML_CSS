# HTML 기본 구조
- html : 문서의 최상위(root) 요소
- head : 문서 메타데이터 요소
    - 문서 제목, 인코딩, 스타일, 외부 파일 로딩 등
    - 일반적으로 브라우저에 나타나지 않는 내용
- body : 문서 본문 요소
    - 실제 화면 구성과 관련된 내용
```
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset = "UTF-8">
    <title>Hello, HTML</title>
</head>
<body>

</body>
</html>
```

## Head 예시
- <title> : 브라우저 상단 타이틀
- < meta > : 문서 레벨 메타데이터 요소
- < link > : 외부 리소스 연결 요소 (CSS 파일, favicon 등)
- <script> : 스크립트 요소 (JavaScript 파일 / 코드)
- <style> : CSS 직접 작성
```
<head>
  <title>HTML 수업</title>
  <meta charset="utf-8">
  <link href="style.css" rel="stylesheet">
  <script src="javascript.js"></script>
  <style>
    p {
      color: black;
    }
   </style>
</head>
```

## head 예시 : Open Graph Protocol
- 메타 데이터를 표현하는 새로운 규약
    - HTML 문서의 메타 데이터를 통해 문서의 정보를 전달
    - 메타 정보에 해당하는 제목, 설명 등을 쓸 수 있도록 정의

## 요소(Element)
### < h1 >contents< /h1 >
- h1 (여는/시작) 태그
- /h1 (닫는/종료)태그
- HTML의 요소는 태그와 내용(contents)으로 구성되어 있다.

- HTML 요소는 시작 태그와 종료 태그 그리고 태그 사이에 위치한 내용으로 구성
    - 요소는 태그로 컨텐츠(내용)를 감싸는 것으로 그 정보의 성격과 의미를 정의
    - 내용이 없는 태그들도 존재(닫는 태그가 없음)
        -br, hr, img, input, link, meta
- 요소는 중첩(nested)될 수 있음
    - 요소의 중첩을 통해 하나의 문서를 구조화
    - 여는 태그와 닫는 태그의 쌍을 잘 확인해야함
        - 오류를 반환하는 것이 아닌 그냥 레이아웃이 깨진 상태로 출력되기 때문에, 디버깅이 힘들어 질 수 있음

## HTML with 개발자 도구
- elements : 해당 요소의 HTML 태그
- 원하는 요소를 선택할 수 있음 (복잡한 형태의 경우 Elements에서 HTML 구조를 추가 탐색)

## 속성(Attribute)
### <a href="https://google.com"></a>
- href (속성명)
- https://google.com (속성값)
- 태그별로 사용할 수 있는 속성이 다르다.

## 속성(attribute) 작성 방식 통일하기
- < a href="https://google.com"></a >
- = 공백은 No!          ""(쌍따옴표) 사용!
- 속성을 통해 태그의 부가적인 정보를 설정할 수 있음
- 요소는 속성을 가질 수 있으며, 경로나 크기와 같은 추가적인 정보를 제공
- 요소의 시작 태그에 작성하며 보통 이름과 값이 하나의 쌍으로 존재
- 태그와 상관없이 사용 가능한 속성(HTML Global Attribute)들도 있음

## HTML Global Attribute
- 모든 HTML 요소가 공통으로 사용할 수 있는 대표적인 속성 (몇몇 요소에는 아무 효과가 없을 수 있음)
    - id : 문서 전체에서 유일한 고유 식별자 지정
    - class : 공백으로 구분된 해당 요소의 클래스의 목록 (CSS ,JS에서 요소를 선택하거나 접근)
    - data-* : 페이지에 개인 사용자 정의 데이터를 저장하기 위해 사용
    - style : inline 스타일
    - title : 요소에 대한 추가 정보 지정
    - tabindex : 요소의 탭 순서

## HTML 코드 예시
```
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset = "UTF-8">
    <title>Hello, HTML</title>
</head>
<body>

</body>
   <!-- 이것은 주적입니다. -->
   <h1>나의 첫번째 HTML</h1>
   <p>이것은 본문입니다.</p>
   <span>이것은 인라인 요소</span>
   <a href="http://www.naver.com">네이버로 이동!!</a>
</body>
</html>
```

## 시맨틱 태그
- HTML 태그가 특정 목적, 역할 및 의미적 가치(semantic value)를 가지는 것
    - 예를 들어 h1 태그는 "이 페이지에서 최상위 제목"인 텍스트를 감싸는 역할(또는 의미)을 나타냄
- Non semantic 요소로는 div, span 등이 있으며 a, form, table 태그들도 시맨틱 태그로 볼 수 있음
- HTML5에서는 기존에 단순히 콘텐츠의 구획을 나타내기 위해 사용한 div 태그를 대처하여 사용하기 위해 의미론적 요소를 담은 태그들이 추가됨
- 대표적인 시맨틱 태크 목록
    - header : 문서 전체나 섹션의 헤더(머리말 부분)
    - nav : 네비게이션
    - aside : 사이드에 위치한 공간, 메인 콘텐츠와 관련성이 적은 콘텐츠
    - section : 문서의 일반적인 구분, 컨텐츠의 그룹을 표현
    - article : 문서, 페이지, 사이트 안에서 독립적으로 구분되는 영역
    - footer : 문서 전체나 섹션의 푸터(마지막 부분)
```
<div>
  <div></div>
</div>
<div>
  <div></div>
  <div></div>
<div>
<div></div>
```
```
<header>
  <nav></nav>
</header>
<section>
  <article></article>
  <article></article>
</section>
<footer></footer>
```

## 시맨틱 태그 사용 해야 하는 이유
- 의미론적 마크업
    - 개발자 및 사용자 뿐만 아니라 검색엔진 등에 의미있는 정보의 그룹을 태그로 표현
    - 단순히 구역을 나누는 것 뿐만 아니라 '의미'를 가지는 태그들을 활용하기 위한 노력
    - 요소의 의미가 명확해지기 때문에 코드의 가독성을 높이고 유지보수를 쉽게 함
    - 검색 엔친 최적화(SEO)를 위해서 메타태크, 시맨틱 태그 등을 통한 마크업을 효과적으로 활용 해야함

## 텍스트로 작성된 코드가 어떻게 웹 사이트가 되는 걸까?
- 렌더링(Rendering)
    - 웹사이트 코드를 사용자가 보게 되는 웹 사이트로 바꾸는 과정

## DOM(Document Object Model) 트리
- 텍스트 파일인 HTML 문서를 브라우저에서 렌더링 하기 위한 구조
    - HTML 문서에 대한 모델을 구성함
    - HTML 문서 내의 각 요소에 접근 / 수정에 필요한 프로퍼티와 메서드를 제공함
```
<body>
  <h1> 웹문서 </h1>
  <ul>
    <li>HTML</li>
    <li>CSS</li>
  </ul>
</body>
```