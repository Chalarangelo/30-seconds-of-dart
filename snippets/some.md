---
title: some
tags: list,beginner
---

Returns `true` if the provided predicate function returns `true` for at least one element in a collection, `false` otherwise.

- Use `Iterable.any()` to test if any elements in the collection return `true` based on `fn`.

```dart
bool some<T>(Iterable<T> itr, bool Function(T) fn) {
  return itr.any(fn);
}
```

```dart
some([0, 1, 2, 0], (x) => x >= 2); // true
```
