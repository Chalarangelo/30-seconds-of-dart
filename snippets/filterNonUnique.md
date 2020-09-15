---
title: filterNonUnique
tags: list,intermediate
---

Filters out the non-unique values in a list.

- Use `Iterable.where()` in combination with `List.indexOf()` and `List.lastIndexOf()` to filter out the non-unique values.

```dart
List<T> filterNonUnique<T>(List<T> lst) {
  return lst.where((i) => lst.indexOf(i) == lst.lastIndexOf(i)).toList();
}
```

```dart
filterNonUnique([1, 2, 2, 3, 4, 4, 5]); // [1, 3, 5]
```
