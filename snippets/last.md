---
title: last
tags: list,beginner
---

Returns the last element in a list.

- Check if `lst` has a non-zero length, use `lst[lst.length - 1]` if possible to return the last element, otherwise return `null`.

```dart
T head<T>(List<T> lst) {
  return lst.length > 0 ? lst[lst.length - 1] : null;
}
```

```dart
head([1, 2, 3]); // 3
head([1]); // 1
head([]); // null
```
