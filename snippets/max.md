---
title: max
tags: math,list,beginner
---

Returns the maximum value in a list of numbers.

- Use `Iterable.reduce()` in combination with `max()` to find the maximum value.

```dart
import 'dart:math';

num max(List<num> nums){
  return nums.reduce(max);
}
```

```dart
max([4, 6, 1, 2, 5]); // 6
```
