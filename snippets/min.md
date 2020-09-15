---
title: min
tags: math,list,beginner
---

Returns the minimum value in a list of numbers.

- Use `Iterable.reduce()` in combination with `min()` to find the minimum value.

```dart
import 'dart:math';

num min(List<num> nums){
  return nums.reduce(math.min);
}
```

```dart
min([4, 6, 1, 2, 5]); // 1
```
