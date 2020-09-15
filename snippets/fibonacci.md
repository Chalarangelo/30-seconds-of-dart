---
title: fibonacci
tags: math,list,beginner
---

Generates a list, containing the Fibonacci sequence, up until the nth term.

- Use `List.generate()` to generate a list with `n` terms, using a function that returns the sum of the last two values, except for the first two.

```dart
List<int> fibonacci(int n) {
  int last = 1;
  int last2 = 0;
  return List<int>.generate(n, (int i) {
    if (i < 2) return i;
    int curr = last + last2;
    last2 = last;
    last = curr;
    return curr;
  });
}
```

```dart
fibonacci(6); // [0, 1, 1, 2, 3, 5]
```
