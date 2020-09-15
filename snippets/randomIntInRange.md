---
title: randomIntInRange
tags: math,utility,random,beginner
---

Returns a random integer in the specified range.

- Use `Random.nextDouble()` to generate a random number between `0.0` and `1.0` and map it to the desired range, using `num.floor()` to make it an integer.
- Omit the optional parameter, `min`, to use a default minimu value of `0`.
- Omit the optional parameter, `max`, to use a default maximum value of `100`.

```dart
import 'dart:math';

int randomIntInRange({int min = 0, int max = 100}) {
  return (Random().nextDouble() * (max - min + 1) + min).floor();
}
```

```dart
randomIntInRange(); // 90
randomIntInRange(min: 10, max: 30); // 23
```
