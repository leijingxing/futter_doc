# kotlin和java的关系

kotlin是java的一个超集，可以直接调用java的代码，也可以调用kotlin的代码，kotlin的代码可以直接编译成java的字节码，也可以编译成js代码，也可以编译成native代码，kotlin的语法和java的语法很像，但是kotlin的语法更加简洁，更加优雅，更加安全，更加高效，更加易用，更加易读，更加易维护，更加易扩展，更加易测试，更加易调试，更加易理�

## kotlin实现java的接口

```kotlin
interface A {
    fun a()
}

class B : A {
    override fun a() {
        println("a")
    }
}
```

## kotlin实现java的抽象类

```kotlin
abstract class A {
    abstract fun a()
}

class B : A() {
    override fun a() {
        println("a")
    }
}
```

## kotlin实现java的枚举类

```kotlin
enum class A {
    A, B, C
}
```

## kotlin实现java的注解

```kotlin
annotation class A
```

## kotlin实现排序

```kotlin
val list = listOf(1, 2, 3, 4, 5)
list.sorted()
```

## kotlin实现线程

```kotlin
thread {
    println("a")
}
```

## kotlin实现lambda表达式

```kotlin
val list = listOf(1, 2, 3, 4, 5)
list.filter { it > 3 }
```

## kotlin实现函数式编程

```kotlin
val list = listOf(1, 2, 3, 4, 5)
list.map { it * 2 }
```

## kotlin实现高阶函数

```kotlin
fun a(f: (Int) -> Int) {
    f(1)
}

a { it * 2 }
```

## kotlin实现函数重载

```kotlin
fun a(i: Int) {
    println("a")
}

fun a(s: String) {
    println("b")
}
```

## kotlin实现函数默认参数

```kotlin
fun a(i: Int = 1) {
    println("a")
}
```

## kotlin实现冒泡排序

```kotlin
    fun bubbleSort(list: List<Int>): List<Int> {
    val result = list.toMutableList()
    for (i in 0 until result.size) {
        for (j in 0 until result.size - i - 1) {
            if (result[j] > result[j + 1]) {
                val temp = result[j]
                result[j] = result[j + 1]
                result[j + 1] = temp
            }
        }
    }
    return result
}
```

## kotlin实现请求网络

```kotlin
val client = OkHttpClient()
val request = Request.Builder().url("https://www.baidu.com").build()
val response = client.newCall(request).execute()
val body = response.body()
val string = body?.string()
```



