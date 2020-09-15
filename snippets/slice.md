---
title: slice
tags: list,intermediate
---

Returns a new list containing the elements between `start` and `end`.
Negative values can be used, indicating an offset from the end of the list.

- Use `num.isNegative` to check if either `start` or `end` are negative and normalize their values.
- Use `List.sublist()` with the normalized values to return the desired list.
- Omit the optional parameter, `end`, to use the length of the list as the default.

```dart
List<T> slice<T>(List<T> lst, int start, [int end]) {
  int _start = start.isNegative ? lst.length + start : start;
  int _end = end != null ? end.isNegative ? lst.length + end : end : lst.length;
  return lst.sublist(_start, _end);
}
```

```dart
List<int> n = [1, 2, 3, 4, 5, 6, 7, 8];

slice(n, 5);      // [6, 7, 8]
slice(n, 1, 3);   // [2, 3]
slice(n, 2, -2);  // [3, 4, 5, 6]
slice(n, -4);     // [5, 6, 7, 8]
slice(n, -6, -2); // [3, 4, 5, 6]
```
