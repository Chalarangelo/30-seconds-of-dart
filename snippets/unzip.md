---
title: unzip
tags: list,intermediate
---

Creates a list of lists, ungrouping the elements in a list produced by [zip](/dart/s/zip).

- Use `List.generate()` twice to generate a list of lists, using the appropriate indexes to get their values from the original list.

```dart
List<List<T>> unzip<T>(List<List<T>> itr) {
  return List.generate(
      itr[0].length, (i) => List.generate(itr.length, (k) => itr[k][i]));
}
```

```dart
unzip([['a', 1, true], ['b', 2, false]]); // [['a', 'b'], [1, 2], [true, false]]
unzip([['a', 1, true], ['b', 2]]); // [['a', 'b'], [1, 2], [true]]
```
