[[Variables]] can be interpolated into strings by using `$` symbol just before the variable name

E.g
```kotlin
fun main() {
	val count: Int = 2
	println("The val here is $count")
}
```

If the value to be interpolated is an expression `{}` can be used to wrap the expression
```kotiln
println("You have ${a + b} messages")
```
