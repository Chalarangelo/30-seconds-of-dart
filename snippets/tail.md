---
title: tail
tags: list,intermediate
---

Returns all the elements of a list except the first one.

- Check if `lst` has the appropriate length, use `List.sublist(1, lst.length)` if possible to return the result, otherwise return `lst`.

```dart
List<T> tail<T>(List<T> lst) {
  return lst.length > 1 ? lst.sublist(1, lst.length) : lst;
}
```

```dart
tail([1, 2, 3]); // [2, 3]
tail([1]); // [1]
tail([]); // []
```
