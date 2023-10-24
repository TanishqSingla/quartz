`val` keyword is used to declare variables

With explicit type casting
```kotlin
fun main() {
	val count: Int = 2
	println(count)
}
```

With implicit type casting
```kotlin
fun main() {
	val count = 2
	println(count)
}
```

## Properties of val
Val cannot be reassigned
> This implies that variables created by `val` declaration are constants and cannot be modified.
```kotlin
val a = 10
a = 20 // Throws Compile Error
```