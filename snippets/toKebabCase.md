---
title: toKebabCase
tags: string,regexp,intermediate
---

Converts a string to kebab case.

- Use `String.replaceAllMapped()` to break the string into words and `String.toLowerCase()` to convert each one to lowercase, using a `RegExp`.
- Use `String.replaceAll()` to replace invalid separator characters (`_` and spaces). with hyphens

```dart
String toKebabCase(String str) {
  return str
      .replaceAllMapped(
          RegExp(
            r'[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*|\b)|[A-Z]?[a-z]+[0-9]*|[A-Z]|[0-9]+'),
          (Match m) => "${m[0].toLowerCase()}")
      .replaceAll(RegExp(r'(_|\s)+'), '-');
}
```

```dart
toKebabCase('camelCase'); // 'camel-case'
toKebabCase('some text'); // 'some-text'
toKebabCase('some-mixed_string With spaces_underscores-and-hyphens'); // 'some-mixed-string-with-spaces-underscores-and-hyphens'
```
