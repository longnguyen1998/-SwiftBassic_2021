# SwiftBassic_2021
Some knowledge of Swift is required.

## Swift introduce
* Swift is programming language developed by __Chris Lattner__ at Apple Inc. 
* Introduced at 2014 WWDC, became open source in 2015.
* Current version is Swift 5.
* Swift can be used to develop application for: iOS, macOS, tvOS, watchOS, Web application.
* And run in multi OS: macOS, Linux base OS.
* Swift is influenced from many other languages like: Objective-C, Rust, Haskell, Ruby, Python, C#, CLU... so Swift will have key features, modern language thinking.
* Swift is safe, syntactic sugar, friendly to new programmers, protocol- oriented programming (interface)...
* Swift can works with Objective C language, and interactive with languages like python, JavaScript...
* Swift is fast, good performance and productivity.

## Expressions
* Swift have same expressions like other programming language.
```swift
#!/usr/bin/env swiftshell

import SwiftShell
var string: String = "Hello Swift"

let years: Int = 2021

func add(_ a: Int, _ b: Int) -> Int{
    return a + b
}

var result = add
```
* Swift not allow increment / decrement operator: i++ / i--.

## Variables & Constants
* There are two way to declare a variable in Swift.
```swift
#!/usr/bin/env swiftshell

import SwiftShell
var string: String = "Hello Swift"

let years: Int = 2021
```
* Variable declared with var can change value (mutable).
* Variable declared with let can’t change value (immutable).
```swift
#!/usr/bin/env swiftshell

import SwiftShell
var string: String = "Hello Swift"
let years: Int = 2021

string = "Welcome Swift"
years = 2222 // Error
```

## Types & Operator
* In swift, when you declare variable, Swift’s compiler will deduce type of var automatically using type inference.
* ```swift
#!/usr/bin/env swiftshell

import SwiftShell
let sampleInt: Int = 1998
let sampleDouble: Double = 1.2
let sampleString: String = "Birthday: \(sampleDouble).\(sampleInt)"

print(type(of: sampleInt))
print(type(of: sampleDouble))
print(type(of: sampleString))
```
* Swift not allow operators between difference file type.
```swift
#!/usr/bin/env swiftshell

import SwiftShell
sampleInt = 2.1 //Error: Cannot assign value of type 'Double' to type 'Int'

let sumWrong = sampleInt + sampleDouble //Error: Differene type
let sumRight = Double(sampleInt) + sampleDouble //sumRight = 1999.2
```
* Swift have 3 type of operators:
✓ Unary operators operate on a single target.
• Unary prefix: !x.
• Unary postfix: x!, x? (optional type).
✓ Binary operators operate on two targets (such as 2 + 3) and are infix because they appear in between their two targets.
✓ Ternary operators operate on three targets. Like C, Swift has only one ternary operator, the ternary conditional operator (a ? b : c).
* Assignment Operator
```swift
#!/usr/bin/env swiftshell

import SwiftShell
var a = 5
let b = 10
a= b
```
* Remainder Operator
✓ 9 % 4 // equals 1
* Nil-Coalescing Operator
✓ a != nil ? a! : b
* Arithmetic Operators ✓ Addition (+)
✓ Subtraction (-)
✓ Multiplication (*) ✓ Division (/)
* Comparison Operators ✓ Equal to (a == b)
✓ Not equal to (a != b)
✓ Greater than (a > b)
✓ Less than (a < b)
✓ Greater than or equal to (a >= b) ✓ Less than or equal to (a <= b)

## Control Flow
* For
```swift
#!/usr/bin/env swiftshell

import SwiftShell
// For in loop
let listChars: Array = ["A", "B", "C", "D", "E", "F", "G"]
for char in listChars {
  print(char)
}

// For in loop with numeric ranges
for index in 1...5 {
  print("\(index) times 5 is \(index * 5)")
}
```
* White
```swift
#!/usr/bin/env swiftshell

import SwiftShell
// While loop
var count = 10
while count > 0 {
  print(count)
  count -= 1
}

// Repeat - while loop
count = 10
repeat {
  count -= 1
  print(count)
} while count > 0
```
* If
```swift
#!/usr/bin/env swiftshell

import SwiftShell
var speed = 100 
if speed >= 100 {
  print("Dangerous, slow down")
} else if speed < 100 && speed > 60 {
  print("Warning, slow down") 
} else {
  print("Safety drive") 
}
```
* Guard
```swift
#!/usr/bin/env swiftshell

import SwiftShell
// Guard (early exit)
let number = Int.random(in: 0...10)
func checkIfValidNumber(_ number: Int) {
guard number % 2 == 0 else {
  print("Nunber not valid")
  return
}
print("Number valid") }
checkIfValidNumber(number)
```
* Switch ( Switch is very powerful statement )
```swift
#!/usr/bin/env swiftshell

import SwiftShell
switch speed {
case 100:
  print("Dangerous, slow down")
case 60:
  print("Warning, slow down")
default:
  print("Safety drive")
}
```
