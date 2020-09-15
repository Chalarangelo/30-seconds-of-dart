---
title: isOdd
tags: math,beginner
---

Returns `true` if the given number is odd, `false` otherwise.

- Checks whether a number is odd or even using the modulo (`%`) operator.
- Returns `true` if the number is odd, `false` if the number is even.

```dart
bool isOdd(num n) {
  return n % 2 != 0;
}
```

```dart
isOdd(3); // true
```

