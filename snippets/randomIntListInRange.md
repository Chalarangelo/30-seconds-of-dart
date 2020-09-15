---
title: randomIntListInRange
tags: math,utility,random,intermediate
---

Returns a a list of `n` random integers in the specified range.

- Use `List.generate()` to generate a list with `n` terms, using a function that returns a random integer between `min` and `max`.
- Omit the optional parameter, `min`, to use a default minimu value of `0`.
- Omit the optional parameter, `max`, to use a default maximum value of `100`.

```dart
import 'dart:math';

List<int> randomIntListInRange(n, {int min = 0, int max = 100}) {
  return List<int>.generate(
      n, (_) => (Random().nextDouble() * (max - min + 1) + min).floor());
}
```

```dart
randomIntListInRange(12, 35, 10); // [ 34, 14, 27, 17, 30, 27, 20, 26, 21, 14 ]
```
