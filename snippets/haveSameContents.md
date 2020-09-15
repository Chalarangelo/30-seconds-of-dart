---
title: haveSameContents
tags: list,intermediate
---

Returns `true` if two lists contain the same elements regardless of order, `false` otherwise.


- Use the plus operator (`+`) to concatenate `a` and `b`, `Iterable.toSet()` to get all the unique values.
- Use a `for..in` loop and compare the occurence count of each value between the two lists.
- Return `false` if any occurence count doesn't match, `true` otherwise.

```dart
bool haveSameContents<T>(List<T> a, List<T> b) {
  for (T v in (a + b).toSet())
    if (a.where((e) => e == v).length != b.where((e) => e == v).length)
      return false;
  return true;
}
```

```dart
haveSameContents([1, 2, 4], [2, 4, 1]); // true
```
