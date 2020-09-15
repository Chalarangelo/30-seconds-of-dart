---
title: mostFrequent
tags: list,intermediate
---

Returns the most frequent element in a list.

- Use `Iterable.toSet()` to get the unique values of the list, `Set.reduce()` to iterate over them and `Iterable.where()` to find the most frequent element.

```dart
T mostFrequent<T>(Iterable<T> itr) {
  return itr.toSet().reduce((i, j) =>
    itr.where((v) => v == i).length > itr.where((v) => v == j).length ? i : j);
}

```

```dart
mostFrequent(['a', 'b', 'a', 'c', 'a', 'a', 'b']); // 'a'
```
