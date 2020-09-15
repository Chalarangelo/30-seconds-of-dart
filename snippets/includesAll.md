---
title: includesAll
tags: list,beginner
---

Returns `true` if all the elements in `values` are included in `itr`, `false` otherwise.

- Use `Iterable.every()` and `Iterable.contains()` to check if all elements of `values` are included in `itr`.

```dart
bool includesAll<T>(Iterable<T> itr, Iterable<T> values) {
  return values.every((v) => itr.contains(v));
}
```

```dart
includesAll([1, 2, 3, 4], [1, 4]); // true
includesAll([1, 2, 3, 4], [1, 5]); // false
```
