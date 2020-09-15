---
title: maxBy
tags: math,list,function,intermediate
---

Returns the maximum value of a list, after mapping each element to a number using the provided function.

- Use `Iterable.map()` to map each element to the numeric value returned by `fn`, `max()` to find the maximum value.

```dart
import 'dart:math';

num maxBy<T>(List<T> lst, num Function(T) fn) {
  return lst.map(fn).reduce(math.max);
}
```

```dart
maxBy([ {'n': 4}, {'n': 2}, {'n': 8}, {'n': 6} ], (o) => o['n']); // 8
```
