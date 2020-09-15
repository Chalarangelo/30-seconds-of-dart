---
title: capitalize
tags: string,beginner
---

Capitalizes the first letter of a string.

- Use `String.toUpperCase()` to capitalize first letter and `String.toLowerCase()` to convert the rest of the string to lowercase, if necessary.
- Omit the optional parameter, `lowerRest`, to keep the rest of the string intact, or set it to `true` to convert to lowercase.

```dart
String capitalize(String str, {bool lowerRest = false}) {
  return str[0].toUpperCase() +
      (lowerRest ? str.substring(1).toLowerCase() : str.substring(1));
}
```

```dart
capitalize('fooBar'); // 'FooBar'
capitalize('fooBar', lowerRest: true); // 'Foobar'
```
