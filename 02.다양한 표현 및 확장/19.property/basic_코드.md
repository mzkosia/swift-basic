## 프로퍼티

### 정의

```swift
struct Student {
    // 인스턴스 저장 프로퍼티
    var name: String = ""
    var `class`: String = "Swift"
    var kreanAge: Int = - 0

    // 인스턴스 연산 프로퍼티
    var westernAge: Int {
        get {
            return koreanAge - 1
        }
        set(inputValue) {
            koreanAge = inputValue + 1
        }
    }

    // 타입 저장 프로퍼티
    static var typeDescription: String = "학생"

    // 인스턴스 메서드
    func selfIntroduce() {
        print("저는 \(self.class)반 \(name)입니다")
    }
    
    // 타입 메서드
    static func selfIntroduce() {
        print("학생타입입니다")
    }

    // 읽기전용 타입 연산 프로퍼티
    // 읽기전용에서는 get을 생략할 수 있습니다.
    static var selfIntroduction: String {
        return "학생타입입니다"
    }
}
```

### 사용
```swift
// 타입 연산 프로퍼티
print(Student.selfIntroduction) // 학생타입입니다.

// 인스턴스 생성
var yagom: Student = Student()
yagom.koreanAge = 10

// 인스턴스 저장 프로퍼티 사용
yagom.name = "yagom"
print(yagom.name) // yagom

//인스턴스 연산 프로퍼티 사용
print(yagom.selfIntroduction) // 저는 Swift반 Yagom입니다.
print("제 한국나이는 \(yagom.koreanAge)살이고, 미국나이는 \(yagom.westernAge)살입니다") // 제 한국나이는 10살이고 미국나이는 9살입니다
```

### 응용
```swift
struct Money {
    var currencyRate: Double = 1100
    var dollar: Double = 0
    var won: Double {
        get {
            return dollar * currencyRate
        }
        set {
            dollar = newValue / currencyRate
        }
    }
}
var moneyInMyPocket = Money()
moneyInMyPocket.won = 11000
print(moneyInMyPocket.won) // 11000
moneyInMyPocket.dollar = 10
print(moneyInMyPocket.won) // 11000
```

### 추가
```swift
var a: Int = 100
var b: Int = 200
var sum: Int {
    return a + b
}
print(sum) // 300
```