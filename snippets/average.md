---
title: average
tags: math,list,beginner
---

Returns the average value of a list of numbers.

Use `iterable.reduce()` to get the sum of all the numbers in a list, divide by `iterable.length` to get the average.

```dart
num average(List<num> nums){
  return nums.reduce((num a, num b) => a + b) / nums.length;
}
```

```dart
average([1, 2, 3, 4]); // 2.5
```
