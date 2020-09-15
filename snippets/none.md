---
title: none
tags: list,beginner
---

Returns `true` if the provided predicate function returns `false` for all elements in a collection, `false` otherwise.

- Use `Iterable.some()` to test if any elements in the collection return `true` based on `fn`.

```dart
bool none<T>(Iterable<T> itr, bool Function(T) fn) {
  return !itr.any(fn);
}
```

```dart
none([0, 1, 3, 0], (x) => x == 2); // true
```
