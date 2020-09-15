---
title: symmetricDifferenceBy
tags: list,math,intermediate
---

Returns the symmetric difference between two lists, after applying the provided function to each list element of both.

- Use `Iterable.toSet()` and `Iterable.map()` to get the unique values in each list after applying `fn` to them.
- Use `Iterable.where()` in combination with `Iterable.contains()` to keep only the values in one list and not the other.
- Finally, use `Iterable.toList()` and `Iterable.addAll()` in combination with the cascade operator (`..`) to return the result.

```dart
List<Y> symmetricdifferenceBy<T,Y>(List<T> a, List<T> b, Y Function(T) fn) {
  final sA = a.map(fn).toSet(), sB = b.map(fn).toSet();
  return a.map((x) => fn(x)).where((x) => !sB.contains(x)).toList()
    ..addAll(b.map((x) => fn(x)).where((x) => !sA.contains(x)));
}
```

```dart
symmetricdifferenceBy([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }, { 'x': 3 }], (v) => v['x']); // [2, 3]
```
