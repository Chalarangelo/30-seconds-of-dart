---
title: words
tags: string,regexp,intermediate
---

Converts a given string into a list of words.

- Use `String.split()` with the supplied `pattern` to convert to a list of strings.
- Use `Iterable.where()` in combination with `String.isNotEmpty` to remove any empty strings.
- Finally, convert to a list using `Iterable.toList()`.
- Omit the optional parameter, `pattern`, to use the default regular expression (non-alphanumeric characters).

```dart
List<String> words(String str, {String pattern = '[^a-zA-Z-]+'}) {
  return str.split(RegExp(pattern)).where((s) => s.isNotEmpty).toList();
}
```

```dart
words('I love dart!!'); // ['I', 'love', 'dart']
words('JavaScript, TypeScript & Dart'); // ['JavaScript', 'TypeScript', 'Dart']
```
