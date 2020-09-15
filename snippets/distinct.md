---
title: distinct
tags: list,beginner
---

Returns the distinct values in a list.

- Use `List.toSet()` to get the distinct values in the list, `Set.toList()` to return them as a list.

```dart
List<T> distinct<T>(List<T> lst) {
  return lst.toSet().toList();
}
```

```dart
distinct([1, 2, 2, 3, 4, 4, 5]); // [1, 2, 3, 4, 5]
```
