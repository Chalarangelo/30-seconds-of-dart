---
title: intersection
tags: list,math,beginner
---

Returns a list of elements that exist in both lists.

- Use `Iterable.toSet()` to get the unique values in `b`.
- Use `Iterable.toSet()`, `Iterable.where()` and `Iterable.contains()` to keep only the values in `a` contained in `b`, `Iterable.toList()` to return the appropriate result.

```dart
List<T> intersection<T>(Iterable<T> a, Iterable<T> b) {
  final s = b.toSet();
  return a.toSet().where((x) => s.contains(x)).toList();
}
```

```dart
intersection([1, 2, 3], [1, 2, 4]); // [1, 2]
```
