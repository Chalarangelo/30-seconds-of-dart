---
title: isAnagram
tags: string,regexp,intermediate
---

Checks if a string is an anagram of another string (case-insensitive, ignores spaces, punctuation and special characters).

- Use `String.toLowerCase()` and `String.prototype.replaceAll()` with an appropriate regular expression to remove unnecessary characters and convert the string to lowercase.
- Use `String.split('')`, `Iterable.sort()`, in combination with the cascade operator (`..`) and `Iterable.join('')` to normalize both strings and check if their normalized forms are equal.

```dart
bool isAnagram(String str1, String str2) {
  String normalize(String str) => (str
          .toLowerCase()
          .replaceAll(RegExp(r'[^a-z0-9]', caseSensitive: false), '')
          .split('')
            ..sort())
      .join('');
  return normalize(str1) == normalize(str2);
}
```

```dart
isAnagram('iceman', 'cinema'); // true
```
