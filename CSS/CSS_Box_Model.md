# CSS Box model
## CSS 원칙
### 모든 요소는 네모(박스모델)이고, 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다. (좌측 상단에 배치)

## Box model
- 모든 HTML 요소는 box 형태로 되어있음
- 하나의 박스는 네 부분(영역)으로 이루어짐
    - margin : 테두리 바깥의 외부 여백 배경색을 지정할 수 없다.
    - border : 테두리 영역
    - padding : 테두리 안쪽의 내부 여백 요소에 적용된 배경색, 이미지는 padding까지 적용
    - content : 글이나 이미지 등 요소의 실제 내용

## Box model 구성 (margin)
```
.margin {
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 30px;
    margin-left: 40px;
    # 상하좌우!
}
```

## Box model 구성 (padding)
```
.margin-padding{
    margin 10px;
    padding: 30px;
    # 상하좌우!
}
```

## Box model 구성 (border)
```
.border{
    border-width: 2px;
    border-style: dashed;
    border-color: black;
    # 상하좌우!
}
```

## Box model 구성 (margin/padding)
- shorthand를 통해서 표현 가능하다.

## Box model 구성 (border)
- border도 shorthand가 있다!

## box model 직접 해보기
```
<body>
  <div class="box">content-box</div>
  <div class="box box-sizing">border-box</div>
</body>
```
```
<style>
  .box {
    width: 100px;
    margin: 10px auto;
    padding: 20px;
    vorder: 1px solid black;
    color: white;
    text-align: center;
    background-color: blueviolet:
  }

  .box-sizing {
    box-sizing: border-box;
    margin-top: 50px;
  }
</style>
```

## box-sizing
- 기본적으로 모든 요소의 box-sizing은 content-box
    - Padding을 제외한 순수 contents 영역만을 box로 지정
- 다만, 우리가 일반적으로 영역을 볼 떄는 border까지의 너비를 100px 보는 것을 원함
    - 그 경우 box-sizing을 border-box로 설정