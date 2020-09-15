---
title: toSnakeCase
tags: string,regexp,intermediate
---

Converts a string to snake case.

- Use `String.replaceAllMapped()` to break the string into words and `String.toLowerCase()` to convert each one to lowercase, using a `RegExp`.
- Use `String.replaceAll()` to replace invalid separator characters (`-` and spaces) with underscores.

```dart
String toSnakeCase(String str) {
  return str
      .replaceAllMapped(
          RegExp(
            r'[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*|\b)|[A-Z]?[a-z]+[0-9]*|[A-Z]|[0-9]+'),
          (Match m) => "${m[0].toLowerCase()}")
      .replaceAll(RegExp(r'(-|\s)+'), '_');
}
```

```dart
toSnakeCase('camelCase'); // 'camel_case'
toSnakeCase('some text'); // 'some_text'
toSnakeCase('some-mixed_string With spaces_underscores-and-hyphens'); // 'some_mixed_string_with_spaces_underscores_and_hyphens'
```
