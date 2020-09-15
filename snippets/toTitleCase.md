---
title: toTitleCase
tags: string,regexp,intermediate
---

Converts a string to title case.

- Use `String.replaceAllMapped()` to break the string into words and capitalize the first letter of each word, using a `RegExp`.
- Use `String.replaceAll()` to replace invalid separator characters (`-` and `_`) with spaces.

```dart
String toTitleCase(String str) {
  return str
      .replaceAllMapped(
          RegExp(
            r'[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*|\b)|[A-Z]?[a-z]+[0-9]*|[A-Z]|[0-9]+'),
          (Match m) =>
            "${m[0][0].toUpperCase()}${m[0].substring(1).toLowerCase()}")
      .replaceAll(RegExp(r'(_|-)+'), ' ');
}
```

```dart
toTitleCase('some_database_field_name'); // 'Some Database Field Name'
toTitleCase('Some label that needs to be title-cased'); // 'Some Label That Needs To Be Title Cased'
toTitleCase('some-package-name'); // 'Some Package Name'
toTitleCase('some-mixed_string with spaces_underscores-and-hyphens'); // 'Some Mixed String With Spaces Underscores And Hyphens'
```
