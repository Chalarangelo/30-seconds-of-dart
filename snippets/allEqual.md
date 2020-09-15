---
title: allEqual
tags: list,beginner
---

Check if all elements in a list are equal.

- Use `Iterable.every()` to check if all the elements of the list are the same as the first one.

```dart
bool allEqual<T>(List<T> itr) {
  return itr.every((i) => i == itr[0]);
}
```

```dart
allEqual([1, 2, 3, 4, 5, 6]); // false
allEqual([1, 1, 1, 1]); // true
```
