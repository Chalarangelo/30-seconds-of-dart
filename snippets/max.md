---
title: max
tags: math,list,beginner
---

Returns the maximum value in a list of numbers.

Use `iterable.reduce()` in combination with `math.max()` to find the maximum value.

```dart
import 'dart:math' as math;

num max(List<num> nums){
  return nums.reduce(math.max);
}
```

```dart
max([4, 6, 1, 2, 5]); // 6
```
