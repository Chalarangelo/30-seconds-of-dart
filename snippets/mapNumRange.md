---
title: mapNumRange
tags: math,beginner
---

Maps a number from one range to another range.

- Returns `n` mapped between `outMin`-`outMax` from `inMin`-`inMax`.

```dart
num mapNumRange(num n, num inMin, num inMax, num outMin, num outMax) {
  return ((n - inMin) * (outMax - outMin)) / (inMax - inMin) + outMin;
}
```

```dart
mapNumRange(5, 0, 10, 0, 100); // 50
```
