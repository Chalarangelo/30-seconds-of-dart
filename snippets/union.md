---
title: union
tags: list,math,beginner
---

Returns every element that exists in any of the two lists once.

- Use the plus operator (`+`) to concatenate `a` and `b`, `Iterable.toSet()` to get the unique values, `Iterable.toList()` to return a list.

```dart
List<T> union<T>(Iterable<T> a, Iterable<T> b) {
  return (a.toList() + b.toList()).toSet().toList();
}
```

```dart
union([1, 2, 3], [4, 3, 2]); // [1, 2, 3, 4]
```
