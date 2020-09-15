---
title: flatten
tags: list,recursion,intermediate
---

Flattens a list.

- Use recursion.
- Use `Iterable.expand()` to combine elements into a single list, calling `flatten` recursively for any elements that are `List`s.

```dart
List<T> flatten<T>(List<T> lst) {
  return lst.expand((e) => e is List ? flatten(e) : [e]).toList();
}
```

```dart
flatten([1, [2], [[3], 4], 5]); // [1, 2, 3, 4, 5]
```
