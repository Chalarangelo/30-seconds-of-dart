---
title: dropRightWhile
tags: list,intermediate
---

Removes elements from the end of a list until the passed function returns `true` and returns the remaining elements.

- Use `List.lastIndexWhere()` with the `test` function to find the last element that returns `true`.
- Return an empty array if there are no matching elements, otherwise use `List.sublist()` to return the remaining elements.

```dart
List<T> dropRightWhile<T>(List<T> lst, bool Function(T) test) {
  int rightIndex = lst.lastIndexWhere(test);
  return rightIndex == -1 ? [] : lst.sublist(0, rightIndex + 1);
}
```

```dart
dropRightWhile([1, 2, 3, 4], (n) => n < 3); // [1, 2]
```
