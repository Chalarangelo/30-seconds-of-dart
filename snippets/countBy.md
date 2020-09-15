---
title: countBy
tags: list,intermediate
---

Groups the elements of a list based on the given function and returns the count of elements in each group.

- Use `Iterable.map()` to map each element to the value returned by `fn`, `Iterable.toSet()` to get the unique values of the list.
- Use `Map.fromIterable()`, `Iterable.where()` and `Iterable.length` to generate a map with the unique values as keys and their frequencies as values.

```dart
Map<Y, int> countBy<T, Y>(Iterable<T> itr, Y Function(T) fn) {
  return Map.fromIterable(itr.map(fn).toSet(),
      value: (i) => itr.where((v) => fn(v) == i).length);
}
```

```dart
countBy(['one', 'two', 'three'], (v) => v.length); // [{3: 2, 5: 1}]
```
