---
title: dropWhile
tags: list,intermediate
---

Removes elements from the start of a list until the passed function returns `true` and returns the remaining elements.

- Use `List.indexWhere()` with the `test` function to find the first element that returns `true`.
- Return an empty array if there are no matching elements, otherwise use `List.sublist()` to return the remaining elements.

```dart
List<T> dropWhile<T>(List<T> lst, bool Function(T) test) {
  int leftIndex = lst.indexWhere(test);
  return leftIndex == -1 ? [] : lst.sublist(leftIndex);
}
```

```dart
dropWhile([1, 2, 3, 4], (n) => n >= 3); // [3, 4]
```
