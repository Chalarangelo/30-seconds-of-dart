---
title: reverseString
tags: string,beginner
---

Reverses a string.

- Use `String.split('')` and `Iterable.reversed` to reverse the order of the runes in the string.
- Use `Iterable.join('')` to combine the runes and get the reversed string.

```dart
String reverseString(String str) {
  return str.split('').reversed.join('');
}
```

```dart
reverseString('foobar'); // 'raboof'
```
