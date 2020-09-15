---
title: fibonacciNumber
tags: math,recursion,beginner
---

Returns the nth term of the Fibonacci sequence.

- Use recursion to calculate the `n`th term in the Fibonacci sequence.

```dart
int fibonacci(int n) {
  if (n <= 0) return 0;
  return n < 2 ? n : (fibonacci(n - 1) + fibonacci(n - 2));
}
```

```dart
fibonacci(6); // 8
```
