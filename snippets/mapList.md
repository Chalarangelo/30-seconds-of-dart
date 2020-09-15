---
title: mapList
tags: list,intermediate
---

Maps the values of a list using a function, where the key-value pairs consist of the value as the key and the mapped value.

- Use `Map.fromIterable()` to generate a map with the original values as keys and their mapped values as values.

```dart
Map<T, Y> mapList<T, Y>(Iterable<T> itr, Y Function(T) fn) {
  return Map.fromIterable(itr, key: (i) => i, value: (i) => fn(i));
}
```

```dart
mapList([1, 2, 3], (a) => a * a); // [{1: 1, 2: 4, 3: 9}]
```
