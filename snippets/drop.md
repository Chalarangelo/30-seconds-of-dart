---
title: drop
tags: list,beginner
---

Returns a new list with `n` elements removed from the left.

- Use `List.sublist()` to remove the specified number of elements from the left.

```dart
List<T> drop<T>(List<T> lst, [int n = 1]) {
  return lst.sublist(n);
}
```

```dart
drop([1, 2, 3]); // [2,3]
drop([1, 2, 3], 2); // [3]
```
