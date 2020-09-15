---
title: everyNth
tags: list,intermediate
---

Returns every nth element in a list.

- Use `List.generate()` to generate a list that fits the number of elements that will be returned, then add every `nth` element to it.

```dart
import 'dart:math';

List<T> everyNth<T>(List<T> lst, int nth) {
  return List.generate(
    (lst.length / nth).floor(), (i) => lst[(i + 1) * nth - 1]);
}
```

```dart
everyNth([1, 2, 3, 4, 5, 6], 2); // [ 2, 4, 6 ]
```
