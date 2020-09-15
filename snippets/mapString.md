---
title: mapString
tags: string,list,function,utility,beginner
---

Creates a string with the results of calling the provided function on every character in the given string.

- Use `String.split('')` and `Iterable.map()` to call the provided function, `fn`, for each character in `str`.
- Use `Iterable.join('')` to recombine the list of runes into a string.

```dart
String mapString(String str, String Function(String c) fn) {
  return str.split('').map(fn).join('');
}
```

```dart
mapString('lorem ipsum', (c) => c.toUpperCase()); // 'LOREM IPSUM'
```
