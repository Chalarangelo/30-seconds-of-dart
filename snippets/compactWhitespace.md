---
title: compactWhitespace
tags: string,regexp,beginner
---

Returns a string with whitespaces compacted.

- Use `String.replaceAll()` with a regular expression to replace all occurrences of 2 or more whitespace characters with a single space.

```dart
String compactWhitespace(String str) {
  return str.replaceAll(RegExp(r'\s{2,}'), ' ');
}
```

```dart
compactWhitespace('Lorem    Ipsum'); // 'Lorem Ipsum'
compactWhitespace('Lorem \n Ipsum'); // 'Lorem Ipsum'
```
