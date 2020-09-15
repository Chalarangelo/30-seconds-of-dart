---
title: compact
tags: list,beginner
---

Removes falsy values from a list.

- Use `Iterable.removeWhere()` in combination with the cascade operator (`..`) to filter out falsy values (`false`, `null`).

```dart
List<T> compact<T>(List<T> lst) {
  return lst..removeWhere((v) => [null, false].contains(v));
}
```

```dart
compact([0, 1, false, 2, 3, 'a', null, 'b']); // [0, 1, 2, 3, 'a', 'b']
```
