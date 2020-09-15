---
title: factorial
tags: math,recursion,beginner
---

Calculates the factorial of an integer.

- Use recursion.
- If `n` is less than or equal to `1`, return `1`.
- Otherwise, return the product of `n` and the factorial of `n-1`.
- Throws an exception if `n` is a negative number.

```dart
int factorial(int n) {
  if (n < 0) throw ('Negative numbers are not allowed.');
  return n <= 1 ? 1 : n * factorial(n - 1);
}
```

```dart
factorial(6); // 720
```
