---
title: bifurcateBy
tags: list,intermediate
---

Splits values into two groups according to a predicate function, which specifies which group an element in the input collection belongs to. 
If the predicate function returns `true`, the collection element belongs to the first group; otherwise, it belongs to the second group.

- Use `Iterable.retainWhere()` and `Iterable.removeWhere()` in combination with the cascade operator (`..`) and `List.from()` to create the appropriate groups using the `filter` function.

```dart
List<List<T>> bifurcateBy<T>(List<T> lst, bool Function(T) filter) {
  return [
    List.from(lst..retainWhere(filter)),
    List.from(lst..removeWhere(filter))
  ];
}
```

```dart
bifurcateBy(['beep', 'boop', 'foo', 'bar'], (x) => x[0] == 'b'); // [['beep', 'boop', 'bar'], ['foo']]
```
