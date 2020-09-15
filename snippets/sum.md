---
title: sum
tags: math,list,beginner
---

Returns the sum value of a list of numbers.

- Use `Iterable.reduce()` to sum all the numbers in a list.

```dart
num sum(List<num> nums){
  return nums.reduce((num a, num b) => a + b);
}
```

```dart
sum([1, 2, 3, 4]); // 10
```
