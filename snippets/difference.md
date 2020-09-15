---
title: difference
tags: list,math,beginner
---

Returns the difference between two lists.

- Use `Iterable.toSet()` to get the unique values in `b`.
- Use `Iterable.where()` in combination with `Iterable.contains()` to keep only the values in `a` not contained in `b`, `Iterable.toList()` to return the appropriate result.

```dart
List<T> difference<T>(Iterable<T> a, Iterable<T> b) {
  final s = b.toSet();
  return a.where((x) => !s.contains(x)).toList();
}
```

```dart
difference([1, 2, 3], [1, 2, 4]); // [3]
```
