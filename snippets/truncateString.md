---
title: truncateString
tags: string,beginner
---

Truncates a string up to a specified length.

- Determine if the string's `length` is greater than `num`.
- Return the string truncated to the desired length, with `'...'` appended to the end or the original string.

```dart
String truncateString(String str, int num) {
  return str.length > num
      ? str.substring(0, num > 3 ? num - 3 : num) + '...'
      : str;
}
```

```dart
truncateString('boomerang', 7); // 'boom...'
```
