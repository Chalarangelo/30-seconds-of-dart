---
title: head
tags: list,beginner
---

Returns the head of a list.

- Check if `lst` has a non-zero length, use `lst[0]` if possible to return the first element, otherwise return `null`.

```dart
T head<T>(List<T> lst) {
  return lst.length > 0 ? lst[0] : null;
}
```

```dart
head([1, 2, 3]); // 1
head([1]); // 1
head([]); // null
```
