---
title: toCamelCase
tags: string,regexp,intermediate
---

Converts a string to camelcase.

- Use `String.replaceAllMapped()` to break the string into words and capitalize the first letter of each word, using a `RegExp`.
- Use `String.replaceAll()` to remove invalid separator characters (`_`, `-` and spaces).
- Finally, use `String.toLowerCase()` and to convert the first letter to lowercase.

```dart
String toCamelCase(String str) {
  String s = str
      .replaceAllMapped(
          RegExp(
            r'[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*|\b)|[A-Z]?[a-z]+[0-9]*|[A-Z]|[0-9]+'),
          (Match m) =>
            "${m[0][0].toUpperCase()}${m[0].substring(1).toLowerCase()}")
      .replaceAll(RegExp(r'(_|-|\s)+'), '');
  return s[0].toLowerCase() + s.substring(1);
}
```

```dart
toCamelCase('some_database_field_name'); // 'someDatabaseFieldName'
toCamelCase('Some label that needs to be camelized'); // 'someLabelThatNeedsToBeCamelized'
toCamelCase('some-javascript-property'); // 'someJavascriptProperty'
toCamelCase('some-mixed_string with spaces_underscores-and-hyphens'); // 'someMixedStringWithSpacesUnderscoresAndHyphens'
```
