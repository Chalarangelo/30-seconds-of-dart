---
title: minBy
tags: math,list,function,intermediate
---

Returns the minimum value of a list, after mapping each element to a number using the provided function.

- Use `Iterable.map()` to map each element to the numeric value returned by `fn`, `min()` to find the minimum value.

```dart
import 'dart:math';

num minBy<T>(List<T> lst, num Function(T) fn) {
  return lst.map(fn).reduce(math.min);
}
```

```dart
minBy([ {'n': 4}, {'n': 2}, {'n': 8}, {'n': 6} ], (o) => o['n']); // 8
```
