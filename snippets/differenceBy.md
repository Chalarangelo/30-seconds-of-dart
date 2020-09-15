---
title: differenceBy
tags: list,math,intermediate
---

Returns the difference between two lists, after applying the provided function to each list element of both.

- Use `Iterable.toSet()` and `Iterable.map()` to get the unique values in `b` after applying `fn` to them.
- Use `Iterable.map()` to apply `fn` to all the values of `a`,  `Iterable.where()` in combination with `Iterable.contains()` to keep only the values in the resulting list not contained in the unique mapped values of `b`, `Iterable.toList()` to return the appropriate result.

```dart
List<Y> differenceBy<T,Y>(Iterable<T> a, Iterable<T> b, Y Function(T) fn) {
  final s = b.map(fn).toSet();
  return a.map((x) => fn(x)).where((x) => !s.contains(x)).toList();
}
```

```dart
differenceBy([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }], (v) => v['x']); // [2]
```
