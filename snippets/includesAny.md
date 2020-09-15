---
title: includesAny
tags: list,beginner
---

Returns `true` if any of the elements in `values` are included in `itr`, `false` otherwise.

- Use `Iterable.any()` and `Iterable.contains()` to check if any elements of `values` are included in `itr`.

```dart
bool includesAny<T>(Iterable<T> itr, Iterable<T> values) {
  return values.any((v) => itr.contains(v));
}
```

```dart
includesAny([1, 2, 3, 4], [2, 9]); // true
includesAny([1, 2, 3, 4], [8, 9]); // false
```
