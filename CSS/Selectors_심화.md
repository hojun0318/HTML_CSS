# Selectors 심화
## 결합자(Combinators)
- 자손 결합자(공백)
    - selectorA 하위의 모든 selectorB 요소
    ```
    <style>
      div span {
        color: red;
      }
    </style>
    ```
- 자식 결합자(>)
    - selectorA 바로 아래의 selectorB 요소
    ```
    <style>
      div > span {
        color: red;
      }
    </style>
    ```
- 일반 형제 결합자(~)
    - selectorA의 형제 요소 중 뒤에 위치하는 selectorB 요소를 모두 선택
    ```
    p ~ span {
        color: red;
    }
    ```
- 인접 형제 결합자(+)
    - selectorA의 형제 요소 중 바로 뒤에 위치하는 selectorB 요소를 선택
    ```
    p + span {
        color: red;
    }
    ```