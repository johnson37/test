# Swift

## 基本类型

数据类型从大的类型上面分成变量和常量
```swift
var myVariable = 42
myVariable = 50
let myConstant = 42
```
每个常量或者变量在Swift中都有一个类型，编译器会进行自动识别，如果无法识别的，可以进行声明，类似于Scala。

### Option type

```swift
let optionalInt: Int? = 9
```

### Option Example
```swift
print (type(of: Int("10")))
```
The return value type is "Optional<Int>"

Once you’re sure that the optional does contain a value, you can access its underlying value by adding an exclamation point (!) to the end of the optional’s name. 

## 数组
```swift
var ratingList = ["Poor", "Fine", "Good", "Excellent"]
ratingList[1] = "OK"
ratingList
```
### Map
```swift
let cast = ["Vivien", "Marlon", "Kim", "Karl"]
let lowercaseNames = cast.map { $0.lowercased() }
// 'lowercaseNames' == ["vivien", "marlon", "kim", "karl"]
let letterCounts = cast.map { $0.count }
// 'letterCounts' == [6, 6, 3, 4]
```

### Reduce
```swift
let numbers = [1, 2, 3, 4]
let numberSum = numbers.reduce(0, { x, y in
    x + y
})
```

### 初始化数组
```swift
let emptyArray = [String]()
```

## Control Flow

### IF
```swift
let number = 23
if number < 10 {
    print("The number is small")
} else if number > 100 {
    print("The number is pretty big")
} else {
    print("The number is between 10 and 100")
}
```

在if语句中使用可选绑定来检查可选类型是否有值。 
```swift
var optionalName: String? = "John Appleseed"
var greeting = "Hello!"
if let name = optionalName {
    greeting = "Hello, \(name)"
}
```

### 问号表达式
```swift
func evenOrOdd(_ number:Int) -> String {
  return number % 2 == 0 ? "Even" : "Odd"
}
```

### Switch

执行完switch匹配的代码块之后，程序将会从switch语句中退出。程序不会继续执行下一个条件项，所以你不需要在每个条件中显式地退出switch语句体（也就是不需要在每个条件中写break）。

Switch语句必须是详尽的。你需要在每个switch中写上default项，除非你已经明确地从上下文中满足了所有的条件－－比如当switch语句在遍历一个枚举的时候。这个要求确保了总会有一个switch条件被执行。

```swift
let vegetable = "red pepper"
switch vegetable {
case "celery":
    let vegetableComment = "Add some raisins and make ants on a log."
case "cucumber", "watercress":
    let vegetableComment = "That would make a good tea sandwich."
case let x where x.hasSuffix("pepper"):
    let vegetableComment = "Is it a spicy \(x)?"
default:
    let vegetableComment = "Everything tastes good in soup."
}
```

### 半开的范围操作符
```swift
var firstForLoop = 0
for i in 0..<4 {
    firstForLoop += i
}
print(firstForLoop)
```

```swift
var secondForLoop = 0
for _ in 0...4 {
    secondForLoop += 1
}
print(secondForLoop)
```

## 函数和方法
```swift
func greet(name: String, day: String) -> String {
    return "Hello \(name), today is \(day)."
}
```
通过在函数名字后面加上一个参数（你传进函数中用以满足参数的值）列表来调用函数。当你调用函数的时候，你传进函数中的第一个参数不需要写出它的参数名字，其他的参数值都需要写出对应的名字。 

```swift
greet("Anna", day: "Tuesday")
greet("Bob", day: "Friday")
greet("Charlie", day: "a nice day")
```

```swift
let exampleString = "hello"
if exampleString.hasSuffix("lo") {
    print("ends in lo")
}
```

## Optional 的用法
```swift
var cnt: Int?

if let num = cnt {
    print("num is \(num)")
}
else
{
    print("cnt is not one Int")
}

```

## 类型转换
### as
as: Guaranteed conversion、 Upcasting
** 字面理解就是有保证的转换，从派生类转换为基类的向上转型 **
```swift
// 将1转成float
let num = 1 as CGFloat
|------------------------
// dog转换到父类animal
class Animal {}
class Dog: Animal {}
let d = Dog()
d as Animal  
```
### as?
as? : *** Optional、 Nil***
```swift
// Dog、Cat和Animal的转换关系
class Animal {}
class Cat: Animal {}
class Dog: Animal {
    var name = "Spot"
}
let dog: Dog? = nil
dog?.name       // 选择调用，返回空值nil
dog!.name       // 强行调用，报错
let animal: Animal = Cat()
animal as? Dog  // 猫转狗失败，返回nil
animal as! Dog  // 猫强行转狗，失败报错
```
### as!
向下类型转换
```swift
// Dog到Animal的转化
class Animal {}
class Dog: Animal {}
let a: Animal = Dog()
a as Dog        // as不能将a转成Dog，即不能向下转换
a as! Dog   // as！能强行将a转成Dog -> Bingo   
```

### Function 中的_

如果您不希望用户输入变量名称，则只需使用下划线。例如，func foo(x: Int, y: Int)被称为foo(6, y: 10)，因此如果您不希望任何调用函数的人必须编写y，您将创建函数func foo(x: Int, _ y: Int)。
如果添加下划线，表明在函数调用时，可以不写形参

## 内连函数
[String](https://developer.apple.com/documentation/swift/string)

## Misc
[Misc](./misc.md)

## Xcode Version
[Xcode Version](https://developer.apple.com/support/xcode/)
[IOS - IPhone](https://www.sohu.com/a/254404579_524654)


## ToDesk

ID: 286 067 586
临时密码：415378

