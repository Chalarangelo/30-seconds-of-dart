---
title: splitLines
tags: string,beginner
---

Splits a multiline string into a list of lines.

- Use `String.split()` and a regular expression to match line breaks and create a list.

```dart
List<String> splitLines(String str) {
  return str.split(RegExp(r'\r?\n'));
}
```

```dart
splitLines('This\nis a\nmultiline\nstring.\n'); // ['This', 'is a', 'multiline', 'string.' , '']
```
