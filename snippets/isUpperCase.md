---
title: isUpperCase
tags: string,beginner
---

Checks if a string is upper case.

- Convert the given string to upper case, using `String.toUpperCase()` and compare it to the original.

```dart
bool isUpperCase(String str) {
  return str == str.toUpperCase();
}
```

```dart
isUpperCase('ABC'); // true
isUpperCase('A3@$'); // true
isUpperCase('aB4'); // false
```
