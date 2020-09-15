---
title: nth
tags: list,beginner
---

Returns the nth element of a list.

- Check if `lst` has a length greater than `n`, use `lst[n]` if possible to return the nth element, otherwise return `null`.
- Omit the second argument, `n`, to get the first element of the list.

```dart
T nth<T>(List<T> lst, [n = 0]) {
  return lst.length > n ? lst[n] : null;
}
```

```dart
nth(['a', 'b', 'c'], 1); // 'b'
```
