---
title: radsToDegrees
tags: math,beginner
---

Converts an angle from radians to degrees.

- Use `pi` and the radian to degree formula to convert the angle from radians to degrees.

```dart
import 'dart:math';

num radsToDegrees(num rad) {
  return (rad * 180.0) / pi;
}
```

```dart
radsToDegrees(pi / 2); // 90
```
