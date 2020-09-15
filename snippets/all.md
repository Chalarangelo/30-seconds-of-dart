---
title: all
tags: list,beginner
---

Returns `true` if the provided predicate function returns `true` for all elements in a collection, `false` otherwise.

- Use `Iterable.every()` to check if all elements in the collection return `true` based on `fn`.

```dart
bool all<T>(Iterable<T> itr, bool Function(T) fn) {
  return itr.every(fn);
}
```

```dart
all([4, 2, 3], (x) => x > 1); // true
```
