## 클로저 고급

```swift

// 기본 클로저 표현

// 클로저를 매개변수로 갖는 함수 calculated(a:b:method:)와 결과값을 저장할 변수 result 선언
func calculate(a: Int, b: Int, method: (Int, Int) -> Int) -> Int {
    return method(a, b)
}
var result: Int

// 후행클로저
result = calculate(a: 10, b: 10) { (left: Int, right: Int) -> Int in
    return left + right
}
print(result) // 20

// 반환타입 생략
// alculate(a:b:method:) 함수의 method 매개변수는 Int 타입을 반환할 것이라는 사실을 컴파일러도 알기 때문에 굳이 클로저에서 반환타입을 명시해 주지 않아도 됨. 대신 in 키워드는 생략할 수 없음
result = calculate(a: 10, b: 10, method: { (left: Int, right: Int) in
    return left + right
})
print(result) // 20
// 후행클로저와 함께 사용할 수도 있습니다
result = calculate(a: 10, b: 10) { (left: Int, right: Int) in
    return left + right
}
print(result) // 20

// 단축 인자이름
result = calculate(a: 10, b: 10, method: {
    return $0 + $1
})
print(result) // 20
// 당연히 후행 클로저와 함께 사용가능
result = calculate(a: 10, b: 10) {
    return $0 + $1
}
print(result) // 20

// 암시적 반환 타입
result = calculate(a: 10, b: 10) {
    $0 + $1
}
print(result) // 20
// 간결하게 한 줄로 표현해 줄 수도 있습니다
result = calculate(a: 10, b: 10) { $0 + $1 }
print(result) // 20

//축약 전
result = calculate(a: 10, b: 10, method: { (left: Int, right: Int) -> Int in
    return left + right
})
//축약 후
result = calculate(a: 10, b: 10) { $0 + $1 }
print(result) // 20

```