---
title: isLowerCase
tags: string,beginner
---

Checks if a string is lower case.

- Convert the given string to lower case, using `String.toLowerCase()` and compare it to the original.

```dart
bool isLowerCase(String str) {
  return str == str.toLowerCase();
}
```

```dart
isLowerCase('abc'); // true
isLowerCase('a3@$'); // true
isLowerCase('Ab4'); // false
```
