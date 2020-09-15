---
title: frequencies
tags: list,intermediate
---

Returns a map with the unique values of a list as keys and their frequencies as the values.

- Use `Iterable.toSet()` to get the unique values of the list.
- Use `Map.fromIterable()`, `Iterable.where()` and `Iterable.length` to generate a map with the unique values as keys and their frequencies as values.

```dart
Map<T, int> frequencies<T>(Iterable<T> itr) {
  return Map.fromIterable(itr.toSet(),
      value: (i) => itr.where((v) => v == i).length);
}
```

```dart
frequencies(['a', 'b', 'a', 'c', 'a', 'a', 'b']); // { a: 4, b: 2, c: 1 }
```
