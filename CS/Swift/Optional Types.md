Forced unwrapping
```swift
var hoge: Int?
10 + hoge // error
10 + hoge! // no error
```

Optional Chaining
```swift
variable?.property
variable?.method()
```

Implicit unwrapping type
```swift
var hoge: Int!
10 + hoge // no error
```

Optional Binding
```swift
var hoge: String?
if let unwrappedHoge = hoge {
	println(unwrappedHoge)
}
else {
	println("no hoge.")
}
```