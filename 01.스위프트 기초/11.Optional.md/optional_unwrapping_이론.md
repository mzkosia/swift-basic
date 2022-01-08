## 옵셔널 추출 

```swift

// optional 예제
func printName(_ name: String) {
    print(name);
}
var myName: String? = nil;

printName(myName) (X) // 전달되는 값이 다르기 때문(옵셔널 - string) 

// if-let (옵셔널 바인딩)
func printName(_ name: String) {
    print(name);
}
var myName: String! = nil;

if let name: String = myName {
    printName(name);
}else{
    print("myName == nil");
}
printName(myName) (X)// name 상수는 if-let 구문에서만 사용가능

var myName: String? = "yagom";
var yourName: String?   = nil;
if let name = myName, let friend = yourName {
    print("\(name) and \(friend)");
}

// force unwrapping
func printName(_ name: String){
    print(name);
}
var myName: String? = "yagom";
printName(myName!);
myName = nil;
prinf(myName!) (X) // 값이 없으므로 런타임 오류

var yourName: String! = nil;
printName(yourName) (X) // nil 값이 전달되기 때문에 런타임 오류

```