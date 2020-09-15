---
title: pad
tags: string,beginner
---

Pads a string on both sides with the specified `padding`, if it's shorter than the specified `length`.

- Use `String.padLeft()` and `String.padRight()` to pad both sides of the given string.
- Omit the optional parameter, `padding`, to use the whitespace as the default padding.

```dart
String pad(String str, int length, {String padding = ' '}) {
  return str
      .padLeft(((str.length + length) / 2).floor(), padding)
      .padRight(length, padding);
}
```

```dart
pad('cat', 8); // '  cat   '
pad(String(42), 6, padding: '0'); // '004200'
pad('foobar', 3); // 'foobar'
```
