---
title: decapitalize
tags: string,beginner
---

Decapitalizes the first letter of a string.

- Use `String.toLowerCase()` to decapitalize first letter and `String.toUpperCase()` to convert the rest of the string to uppercase, if necessary.
- Omit the optional parameter, `upperRest`, to keep the rest of the string intact, or set it to `true` to convert to uppercase.

```dart
String capitalize(String str, {bool upperRest = false}) {
  return str[0].toUpperCase() +
      (upperRest ? str.substring(1).toLowerCase() : str.substring(1));
}
```

```dart
capitalize('FooBar'); // 'fooBar'
capitalize('FooBar', upperRest: true); // 'fOOBAR'
```
