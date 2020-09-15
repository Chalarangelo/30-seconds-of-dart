---
title: symmetricDifference
tags: list,math,intermediate
---

Returns the symmetric difference between two lists, without filtering out duplicate values.

- Use `Iterable.toSet()` to get the unique values in each list.
- Use `Iterable.where()` in combination with `Iterable.contains()` to keep only the values in one list and not the other.
- Finally, use `Iterable.toList()` and `Iterable.addAll()` in combination with the cascade operator (`..`) to return the result.

```dart
List<T> symmetricDifference<T>(List<T> a, List<T> b) {
  final sA = a.toSet(), sB = b.toSet();
  return a.where((x) => !sB.contains(x)).toList()
    ..addAll(b.where((x) => !sA.contains(x)));
}
```

```dart
symmetricDifference([1, 2, 3], [1, 2, 4]); // [3, 4]
symmetricDifference([1, 2, 2], [1, 3, 1]); // [2, 2, 3]
```
