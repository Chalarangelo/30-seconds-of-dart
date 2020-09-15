---
title: sumBy
tags: math,list,function,intermediate
---

Returns the sum of a list, after mapping each element to a number using the provided function.

- Use `Iterable.map()` to map each element to the numeric value returned by `fn`, `Iterable.reduce()` to sum the values.

```dart
num sumBy<T>(List<T> lst, num Function(T) fn) {
  return lst.map(fn).reduce((num a, num b) => a + b);
}
```

```dart
sumBy([ {'n': 4}, {'n': 2}, {'n': 8}, {'n': 6} ], (o) => o['n']); // 20
```
