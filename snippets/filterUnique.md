---
title: filterUnique
tags: list,intermediate
---

Filters out the unique values in a list.

- Use `Iterable.where()` in combination with `List.indexOf()` and `List.lastIndexOf()` to filter out the unique values.

```dart
List<T> filterUnique<T>(List<T> lst) {
  return lst.where((i) => lst.indexOf(i) != lst.lastIndexOf(i)).toList();
}
```

```dart
filterUnique([1, 2, 2, 3, 4, 4, 5]); // [2, 2, 4, 4]
```
