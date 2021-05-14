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

## function patterns
semantic: **fun**

- Type of function that don't return value: **Unit** (like void in other langs):
```kotlin
fun printMessage(message: String): Unit {
    println(message)
}
```