### 매개변수
```swift

// 매개변수 기본값
func greeting(friend:String, me: String = "yagom") {
    print("Hello \(friend)! I'm \(me)");
}
greeting(friend: "hana");
greeting(friend: "john", me: "eric");

// 전달인자 레이블
func greeting(to friend:String, from me: String = "yagom") {
    print("Hello \(friend)! I'm \(me)");
}
greeting(to: "hana", from: "yagom");

// 가변 매개변수
func sayHelloToFriends(me: String, friends: String...) -> String{
    return "Hello \(friends)! I'm \(me)!";
}
printf(sayHelloToFriends(me: "yagom", friends: "hana", "eric", "wing"))
printf(sayHelloToFriends(me: "yagom" ))

```

## 데이터 타입
```swift

// 함수의 타입표현
var someFunction: (String, String) -> Void = greeting(to:from:);
someFunction = greeting(friend:me:);
someFunction("eric", "yagom");

func runAnother(function: (String, String) -> Void){
    function("jenny", "mike");
}

runAnother(function: greeting(friend:me:));
runAnother(function: someFunction);

```