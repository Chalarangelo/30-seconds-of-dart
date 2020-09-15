---
title: groupBy
tags: list,intermediate
---

Groups the elements of a list based on the given function.

- Use `Iterable.map()` to map each element to the value returned by `fn`, `Iterable.toSet()` to get the unique values of the list.
- Use `Map.fromIterable()`, `Iterable.where()` and `Iterable.toList()` to generate a map with the unique values as keys and the list elements as values.

```dart
Map<Y, List<T>> groupBy<T, Y>(Iterable<T> itr, Y Function(T) fn) {
  return Map.fromIterable(itr.map(fn).toSet(),
      value: (i) => itr.where((v) => fn(v) == i).toList());
}
```

```dart
groupBy(['one', 'two', 'three'], (v) => v.length); // {3: ['one', 'two'], 5: ['three']}
```
