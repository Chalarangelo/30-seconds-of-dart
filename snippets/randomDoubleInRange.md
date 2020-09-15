---
title: randomDoubleInRange
tags: math,utility,random,beginner
---

Returns a random double in the specified range.

- Use `Random.nextDouble()` to generate a random number between `0.0` and `1.0` and map it to the desired range.
- Omit the optional parameter, `min`, to use a default minimu value of `0.0`.
- Omit the optional parameter, `max`, to use a default maximum value of `1.0`.

```dart
import 'dart:math';

double randomDoubleInRange({double min = 0.0, double max = 1.0}) {
  return Random().nextDouble() * (max - min + 1) + min;
}
```

```dart
randomDoubleInRange(); // 0.719213632334785
randomDoubleInRange(min: 2.4, max: 9.8); // 6.21315328537085
```
