# CSS Position
- 무선 상에서 요소의 위치를 지정
- static: 모든 태그의 기본 값(기준 위치)
 - 일반적인 요소의 배치 순서에 따름(좌측 상단)
 - 부모 요소 내에서 배치될 때는 부모 요소의 위치를 기준을 배치 됨
- 아래는 좌표 프로퍼티(top, bottom, left, right)를 사용하여 이동 가능
    - relative
    - absolute
    - fixed
    - sticky

- 1 relative : 상대 위치
    - 자기 자신의 static 위치를 기준으로 이동 (normal flow 유지)
    - 레이아웃에서 요소가 차지하는 공간은 static일 때와 같음 (normal position 대비 offset)
- 2 absolute : 절대 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음 (normal folow에서 벗어남)
    - static이 아닌 가장 가까이 있는 부모/조상 요소를 기준으로 이동 (없는 경우 브라우저 화면 기준으로 이동)
- 3 fixed : 고정 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음 (normal flow에서 벗어남)
    - 부모 요소와 관게없이 viewpoint를 기준으로 이동
        - 스크롤 시에도 항상 같은 곳에 위치함
- 4 sticky : 스크롤에 따라 static -> fixed로 변경
    - 속성을 적용한 박스는 평소에 문서 안에서 position: static 상태와 같이 일반적인 흐름에 따르지만 스크롤 위치가 임계점에 이르면 position: fixed와 같이 박스를 화면에 고정할 수 있는 속성

## static
```
div {
    height: 100px;
    width: 100px;
    background-color: #9775fa;
    color: black;
    line-height: 100px;
    text-align: center;
}
```

## relative
```
.relative {
    position: relative;
    top: 100px;     # 기존 위치(normal position)대비 offset
    left: 100px;   
}
```

## absolute
```
.parent {
    position: relative;
}

.absolute-child {
    position: absolute;     # noraml flow에서 벗어나 부모/조상 요소를 기준으로 위치
    top: 50px;
    left: 50px;
}
```

## fixed
```
# normal flow에서 벗어나 Viewport 기준으로 위치
.fixed {
    position: fixed;
    bottom: 0;
    right: 0;
}
```

## absolute vs relative
- absolute는 normal flow에서 벗어남 즉, 다음 블록 요소가 좌측 상단으로 붙음
- relative는 normal flo 유지, 실제 위치는 그대로, 사람 눈에만 이동

## absolute는 언제 쓸까요?
- 특정 영역 위에 존재
- CSS 기본 원칙인 좌측 상단에 배치되지 않음
- **부모**를 기준으로 가운데 위치

## fixed는 언제 쓸까요?
- 브라우저 기준으로 위치
- CSS 기본 원칙인 좌측 상단에 배치되지 않음
- **브라우저**를 기준으로 우측 하단에 배치

## psition sticky
- sticky : 스크롤에 따라 static -> fixed로 변경
    - 속성을 적용한 박스는 평소에 무서 안에서 position: static 상태와 같이 일반적인 흐름에 따르지만, 스크롤 위치가 임계점에 이르면 position: fixed와 같이 박스를 화면에 고정할 수 있는 속성

## CSS 원칙
- CSS 원칙 I, II : Normal flow
    - 모든 요소는 네모(박스모델), 좌측 상단에 배치
    - Display에 따라 크기와 배치가 달라짐
- CSS 원칙 III
    - **Position으로 위치의 기준을 변경**
        - relative : 본인의 원래 위치
        - absolute : 특정 부모의 위치
        - fixed : 화면의 위치
        - sticky : 기본적으로 static이나 스크롤 이동에 따라 fixed로 변경