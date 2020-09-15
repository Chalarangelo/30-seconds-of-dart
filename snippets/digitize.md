---
title: digitize
tags: math,list,beginner
---

Converts an integer to a list of digits.

- Use string interpolation to convert the integer to a string, `String.split('')` to convert it into a list.
- Use `Iterable.map()` and `int.parse()` to transform each value to an integer, `Iterable.toList()` to return a list.

```dart
List<int> digitze(int n) {
  return "${n}".split('').map((s) => int.parse(s)).toList();
}
```

```dart
digitize(123); // [1, 2, 3]
```
