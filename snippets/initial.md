---
title: initial
tags: list,intermediate
---

Returns all the elements of a list except the last one.

- Check if `lst` has the appropriate length, use `List.sublist(0, lst.length - 1)` if possible to return the result, otherwise return `lst`.

```dart
List<T> initial<T>(List<T> lst) {
  return lst.length > 1 ? lst.sublist(0, lst.length - 1) : lst;
}
```

```dart
initial([1, 2, 3]); // [1, 2]
initial([1]); // [1]
initial([]); // []
```
