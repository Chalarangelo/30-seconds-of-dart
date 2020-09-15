---
title: intersectionBy
tags: list,math,intermediate
---

Returns a list of elements that exist in both lists, after applying the provided function to each element of both.

- Use `Iterable.toSet()` and `Iterable.map()` to get the unique values in `b` after applying `fn` to them.
- Use `Iterable.map()` to apply `fn` to all the values of `a`, `Iterable.toSet()`, `Iterable.where()` and `Iterable.contains()` to keep only the values in the resulting list contained in the unique mapped values of `b`, `Iterable.toList()` to return the appropriate result.

```dart
List<Y> intersectionBy<T, Y>(Iterable<T> a, Iterable<T> b, Y Function(T) fn) {
  final s = b.map(fn).toSet();
  return a.toSet().map((x) => fn(x)).where((x) => s.contains(x)).toList();
}
```

```dart
intersectionBy([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }], (v) => v['x']); // [1]
```
