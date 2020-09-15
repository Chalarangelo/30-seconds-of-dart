---
title: sample
tags: list,random,beginner
---

Returns a random element from a list.

- Use `Random.nextInt()` to generate a random integer between `0` and `lst.length` and return the list element at that index.

```dart
import 'dart:math';

T sample<T>(List<T> lst) {
  return lst[Random().nextInt(lst.length)];
}
```

```dart
sample([3, 7, 9, 11]); // 9
```
