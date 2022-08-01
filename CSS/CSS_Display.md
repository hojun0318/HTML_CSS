# CSS Display
## CSS 원칙 II
### 모든 요소는 네모(박스모델)이고, 좌측상단에 배치
### Display에 따라 크기와 배치가 달라진다.

## 대표적으로 활용되는 Display
- display: block
    - 줄 바꿈이 일어나는 요소
    - 화면 크기 전체의 가로 폭을 차지한다.
    - 블록 레벨 요소 안에 인라인 레벨 요소가 들어갈 수 있음
- dispaly: inline
    - 줄 바꿈이 일어나지 않는 행의 일부 요소
    - content 너비만큼 가로 폭을 차지한다.
    - width, height, margin-top, margin-bottom을 지정할 수 없다.
    - 상하 여백은 line-height로 지정한다.

## 블록 레벨 요소와 인라인 레벨 요소
- 블록 레벨 요소와 인라인 레벨 요소 구분(HTML 4.1까지)
- 대표적인 블록 레벨 요소
    - div / ul, il, li / p / hr / form 등
- 대표적인 인라인 레벨 요소
    - span / a / img / inputm, lable / b, em, i, strong 등

## block
- block의 기본 너비는 가질 수 있는 너비의 100%
- 너비를 가질 수 없다면 자동으로 부여되는 margin

## inline
- inline의 기본 너비는 컨텐츠 영역만큼

## Display
- display: inline-block
    - block과 inline 레벨 요소의 특징을 모두 가짐
    - inline처럼 한 줄에 표시할 수 있고, block처럼 width, height, margin 속성을 모두 지정할 수 있음
- display: none
    - 해당 요소를 화면에 표시하지 않고, 공간조차 부여되지 않음
    - 이와 비슷한 visibility: hidden은 해당 요소가 공간은 차지하나 화면에 표시만 하지 않는다.
- 이외 다양한 display 속성은 https://developer.mozilla.org/ko/docs/Web/CSS/display

## 직접 확인해보기
```
<body>
  <h1>나는 block입니다</h1>
  <div>block</dib>
  <p>나는 <span>인라인</span>속성입니다.</p>
  <hr>
  <h2>display none vs visibility hidden</h2>
  <div>1</div>
  <div class="none">2</div>
  <div class="hidden">3</div>
  <div>4</div>
</body>
```
```
<style>
  div {
    width: 100px;
    height: 100px;
    border: 2px solid black;
    background-color: crimson;
  }

  .none {
    display: none;
  }

  .hidden {
    visibility: hidden;
  }
</style>
```