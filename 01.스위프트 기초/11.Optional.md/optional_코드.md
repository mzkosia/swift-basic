## 옵셔널

```swift

let optionalValue: Optional<Int> = nil;
let optionalValue: Int? = nil;

// 암시적 추출 옵셔널 !
var optionalValue: Int! = 100;
swich optionalValue {
    case .none:
        print("This optional variable is nil");
    case .some:
        print("Value is \(value)");
}

// ! 예제
optionalValue = optionalValue + 1;
optionalValue = nil;
optionalValue = optionalValue + 1; (X)

// 옵셔널 ?
var optionalValue: Int? = 100;
swich optionalValue {
    case .none:
        print("This optional variable is nil");
    case .some:
        print("Value is \(value)");

// ? 예제
// 옵셔널과 일반 값은 다른 타입이므로 연산불가
optionalValue = optionalValue + 1; (X)

```