# learn-kotlin

## Hello World and basics

version **1.3 >**:
```kotlin
package org.kotlinlang.play

fun main() {
    println("Hello, World!")
}

```

version **1.3 <**:
```kotlin
fun main(args: Array<String>) {
    println("Hello, World!")
}
```

## Function patterns
semantic: **fun**

- Type of function that don't return value: **Unit** (like void in other langs):
```kotlin
fun printMessage(message: String): Unit {
    println(message)
}
```

- Single-expression function (link a short function):
```kotlin
fun multiply(x: Int, y: Int) = x * y // return integer (inferred)
```

- Named arguments
```kotlin
fun printMessageWithPrefix(message: String, prefix: String = "Info") {  // 2
    println("[$prefix] $message")
}

fun main() {
    printMessageWithPrefix(prefix = "Log", message = "Hello") // named arguments change order of arguments. Prints: [Log] Hello
}
```

- Infix Functions
Tips: thinking infix will be like a operator. // 2 + 2 = operand OPERATOR operand (expand example below)
<details>
<summary>Click to expand code from <a href="https://play.kotlinlang.org/byExample/01_introduction/02_Functions" target="_blank">Kotlin Doc</a></summary>
<p>

```kotlin
    fun main() {

    infix fun Int.times(str: String) = str.repeat(this)
    println(2 times "Bye ") // Bye Bye 

    val pair = "Ferrari" to "Katrina"
    println(pair) // (Ferrari, Katrina)

    infix fun String.onto(other: String) = Pair(this, other)
    val myPair = "McLaren" onto "Lucas"
    println(myPair) // (McLaren, Lucas)

    val sophia = Person("Sophia")
    val claudia = Person("Claudia")
    sophia likes claudia
    }

    class Person(val name: String) {
    val likedPeople = mutableListOf<Person>()
    infix fun likes(other: Person) { likedPeople.add(other) }
    }
```
</p>
</details>