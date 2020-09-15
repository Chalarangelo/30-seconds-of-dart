---
title: isPalindrome
tags: string,intermediate
---

Returns `true` if the given string is a palindrome, `false` otherwise.

- Use `String.toLowerCase()` to convert the given string to lowercase, `String.replaceAll()` to remove non-alphanumeric characters.
- Use `String.split('')`, `Iterable.reversed` and `Iterable.join('')` to reverse it and compare it to the unreversed string.

```dart
bool isPalindrome(String str) {
  String s = str.toLowerCase().replaceAll(RegExp(r'[\W_]'), '');
  return s == s.split('').reversed.join('');
}
```

```dart
isPalindrome('taco cat'); // true
```
