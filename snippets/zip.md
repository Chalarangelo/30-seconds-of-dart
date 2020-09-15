---
title: zip
tags: list,intermediate
---

Creates a list of elements, grouped based on the position in the original lists.

- Use `List.generate()` to generate a list, using `Iterable.map()`, `Iterable.reduce()` and `max()` to get the longest sublist.
- Use `List.generate()` inside the iterator to generate the sublists, using the appropriate indexes to get their values from the original list.

```dart
import 'dart:math';

List<List<T>> zip<T>(List<List<T>> itr) {
  return List.generate(
      itr.map((x) => x.length).reduce(max),
      (i) => List.generate(
          itr.length, (k) => itr[k].length > i ? itr[k][i] : null));
}
```

```dart
zip([['a', 'b'], [1, 2], [true, false]]); // [['a', 1, true], ['b', 2, false]]
zip([['a'], [1, 2], [true, false]]); // [['a', 1, true], [null, 2, false]]
```
