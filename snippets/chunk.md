---
title: chunk
tags: list,intermediate
---

Chunks a list into smaller lists of the specified size.

- Use `List.generate()` to generate a list that fits the number of chunks that will be produced.
- Use `List.sublist()` to map each element of the new list to a chunk the length of `size`.
- If the original `list` can't be split evenly, the final chunk will contain the remaining elements.

```dart
import 'dart:math';

List<List<T>> chunk<T>(List<T> lst, int size) {
  return List.generate((lst.length / size).ceil(),
      (i) => lst.sublist(i * size, min(i * size + size, lst.length)));
}
```

```dart
chunk([1, 2, 3, 4, 5], 2); // [[1, 2], [3, 4], [5]]
```
