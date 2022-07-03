---
layout: post
title: 변수
date: 2022-07-02
parent: 기본 문법
grand_parent: 코틀린
nav_order: 1
---

## 변수 선언

### 불변 변수

키워드 `val`(value)[밸]를 사용하여 불변 변수를 선언한다. 불변 변수는 한 번 값을 초기화한 후에는 값을 재할당할 수 없다. (read-only)

```kotlin
val a: Int = 1
```

### 가변 변수

키워드 `var`(variable)[바]를 사용하여 가변 변수를 선언한다. 가변 변수는 최초에 값을 초기화하고 값을 재할당할 수 있다.

```kotlin
var b: Int = 1
x += 1
```

### 변수 선언과 동시에 초기화 하는 경우 타입은 생략할 수 있다.

코틀린 컴파일러가 변수에 할당되는 값을 통해서 타입을 자동으로 추론해준다.

```kotlin
var b = 1
```

### 변수 선언 후 초기화하기

변수를 먼저 선언하고 그 이후에 변수에 값을 할당한다.

```kotlin
val c: Int
c = 3
```

{: .warn }
타입을 명시해주지 않으면 컴파일 오류가 발생한다.

## 탑 레벨 변수

클래스나 함수 내부에서 변수를 생성하지 않고 파일 최상위에 변수를 선언할 수 있다. 이때, 변수는 "**탑 레벨에 위치한다.**"라고 한다.

```kotlin
var x = 5

fun main() {
    x += 1
    println(x) // 6
}
```