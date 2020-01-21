---
title: averageBy
tags: math,list,function,intermediate
---

Returns the average of a list, after mapping each element to a number using the provided function.

Use `iterable.map()` to map each element to the numeric value returned by `fn`, `iterable.reduce()` to sum the values, divide by `iterable.length` to get the average.

```dart
num averageBy<T>(List<T> lst, num Function(T) fn) {
  return lst.map(fn).reduce((num a, num b) => a + b) / lst.length;
}
```

```dart
averageBy([ {'n': 4}, {'n': 2}, {'n': 8}, {'n': 6} ], (o) => o['n']); // 5
```
