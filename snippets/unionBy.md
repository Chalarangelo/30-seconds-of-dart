---
title: unionBy
tags: list,math,intermediate
---

Returns every element that exists in any of the two lists once, after applying the provided function to each element of both.

- Use `Iterable.toSet()` and `Iterable.map()` to get the unique values in `a` after applying `fn` to them.
- Use `Iterable.map()` to apply `fn` to all the values of `b`, `Iterable.toSet()`, `Iterable.where()` and `Iterable.contains()` to keep only the values in the resulting list contained in the unique mapped values of `a`, `Iterable.toList()` to return the appropriate result.
- Finally, use the plus operator (`+`) to concatenate the two lists and return the result.

```dart
List<Y> unionBy<T, Y>(Iterable<T> a, Iterable<T> b, Y Function(T) fn) {
  final sA = a.map(fn).toSet().toList();
  final sB = b.map(fn).toSet().where((x) => !sA.contains(x)).toList();
  return sA + sB;
}
```

```dart
unionBy([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }], (v) => v['x']); // [2, 1]
```
