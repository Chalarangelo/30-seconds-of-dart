---
title: fibonacciNumber
tags: math,beginner
---

Returns the nth Fibonacci number.

Use recurtion to calculate the nth Fibonacci number. Returns (0) for negative numbers.

```dart
int fibonacci(int n) {
  if ( n > 0 ) {
    return n < 2 ? n : (fibonacci(n - 1) + fibonacci(n - 2));
  } else {
    return 0;
  }
}
```

```dart
fibonacci(6); // 8
```
