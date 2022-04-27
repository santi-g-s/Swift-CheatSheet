# Swift Cheat Sheet

## Table of Contents

1. [Simple Types](#simple-types)
2. [Complex Types](#complex-types)

## Simple Types

   ### Variables

   - You can *mutate* the values freely

```swift
var str = "Hello, playground"

str = "Goodbye"
```

   ### String and Integers

   - Store whole numbers with `Int`

```swift
var age: Int = 38
var population: Int = 8_000_000 //undersores ignored by compiler

var name: String = "John"
```

   ### Multi-line string

   - Triple quotation marks must be *on their own line*

```swift
var str1 = """
This goes
over multiple
lines
"""
```

   ### Doubles & Booleans

   > Double: *Double-precision floating-point number*

```swift
var pi = 3.141
```

   > Boolean: *hold either true or false*

```swift
var awesome = true
```

   ### String Interpolation

   - Place variables inside your string

```swift
var score = 85
var str = "Your score was \(score)"
```

   ### Constants

   - The `let` keyword creates *constants*, which are values that can be set once and never again

```swift
let taylor = "swift"
```

   ### Type Annotations

   - Swift uses **type inference** to *infer* what type a value should have. If you want to be explicit:

```swift
let album: String = "Reputation"
let year: Int = 1989
let height: Double = 1.78
let taylorRocks: Bool = true
```

## Complex Types

   ### Arrays

   - Collections of values that are stored as a single value

```swift
let john = "John Lennon"
let paul = "Paul McCartney"
let george = "George Harrison"
let ringo = "Ringo Starr"

let beatles = [john, paul, george, ringo]
```

   - Read values by writing number inside brackets

```swift
beatles[1] //"Paul McCartney"
```

   ### Sets

   - Like Arrays but with two differences:
      1. Not ordered
      2. All items must be unique

```swift
let colors = Set(["red", "green", "blue"])
```

   ### Tuples

   - Tuples allow you to store several values together in a single value
   - Different from arrays for 3 reasons:
      1. Tuples are of fixed size
      2. You can’t change the type of items in a tuple
      3. You can access items in a tuple using numerical positions or by naming them, but Swift won’t let you read numbers or names that don’t exist.

```swift
var name = (first: "Taylor", last: "Swift")

//Access using numerical position
name.0

//Access using name
name.first
```

   ### Dictionaries

   - Stores a collection of values using a unique *key* to access each one.

```swift
let heights = [
    "Taylor Swift": 1.78,
    "Ed Sheeran": 1.73
]
```

   - To read values out of a dictionary

```swift
heights["Taylor Swift"]
```

   ### Dictionary Default Values

   - If you try to read a value from a dictionary using a key that doesn’t exist, Swift will send you back `nil`
   - We can provide the dictionary with a default value to use if we request a missing key.

```swift
let favoriteIceCream = [
    "Paul": "Chocolate",
    "Sophie": "Vanilla"
]

//Default Values:
favoriteIceCream["Charlotte", default: "Unknown"]
```

   ### Creating Empty Collections

```swift
//Arays
var results = [Int]()
var results = Array<Int>()

//Dictionarys
var teams = [String: String]()
var scores = Dictionary<String, Int>()

//Sets
var words = Set<String>()
```

   ### Enumerations

