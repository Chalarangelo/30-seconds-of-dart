---
title: dropRight
tags: list,beginner
---

Returns a new list with `n` elements removed from the right.

- Use `List.sublist()` to remove the specified number of elements from the right.

```dart
List<T> dropRight<T>(List<T> lst, [int n = 1]) {
  return lst.sublist(0, lst.length - n);
}
```

```dart
dropRight([1, 2, 3]); // [1,2]
dropRight([1, 2, 3], 2); // [1]
```
