## 반복문
```swift
var integers = [1,2,3];
let people = ["yagom": 10, "yagom": 15,"yagom": 12,]

// for-in (like foreach)
for integer in integers {
    print(integer);
}
// dictionary (key, value(튜플타입)) for in
for (name, age) in people {
    print("\(name): \(age)");
}

// while
while integers.count > 1 {
    integers.removeLast();
}

// repeat-while
repeat{
    integers.removeLast();
}while integers.count > 0

```