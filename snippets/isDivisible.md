---
title: isDivisible
tags: math,beginner
---

Checks if the first integer argument is divisible by the second one.

- Use the modulo operator (`%`) to check if the remainder is equal to `0`.

```dart
bool isDivisible(int dividend, int divisor) {
  return dividend % divisor == 0;
}
```

```dart
isDivisible(6, 3); // true
```
