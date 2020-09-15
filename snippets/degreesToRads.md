---
title: degreesToRads
tags: math,beginner
---

Converts an angle from degrees to radians.

- Use `pi` and the degree to radian formula to convert the angle from degrees to radians.

```dart
import 'dart:math';

num degreesToRads(num deg) {
  return (deg * pi) / 180.0;
}
```

```dart
degreesToRads(90.0); // ~1.5708
```
