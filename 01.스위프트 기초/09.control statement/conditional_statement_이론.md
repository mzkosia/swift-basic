## 조건문

### if-else 구문
if뒤의 조건 값에는 항상 Boolean 타입의 값만 위치
조건은 감싸는 소괄호는 선택사항 중괄호 생략불가

```swift
if 조건 {
     /* 실행 구문 */
} else if 조건 {
    /* 실행 구문 */
} else {
    /* 실행 구문 */
}
```

### switch 구문
다른 언어에 비교해서 활용도가 높음
범위 연산자 "..<", "..."
기본적으로 사용하단 정수타입의 값만 아니라 대부분 기본타입 지원

다양한 패던과 응용이 가능
 [Swift Programming Language Reference의 패턴](https://docs.swift.org/swift-book/index.html)

각각의 case 내부에는 실행가능한 코드가 반드시 위치
 
매우 한정적인 값(ex. enum의 case 등)이 비교값이 아닌 한 default 구문은 반드시 작성
 
명시적 break를 하지 않아도 자동으로 case 마다 break 가능

fallthrough 키워드를 사용하여 break를 무시

쉼표(,)를 사용하여 하나의 case에 여러 패턴을 명시

```swift

switch 비교값 {
case 패턴:
    /* 실행 구문 */
default:
    /* 실행 구문 */
}

```

