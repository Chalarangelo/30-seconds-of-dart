---
title: removeNonASCII
tags: string,regexp,intermediate
---

Removes non-printable ASCII characters.

- Use `String.replaceAll()` with a regular expression to remove non-printable ASCII characters.

```dart
String removeNonASCII(String str) {
  return str.replaceAll(RegExp(r'[^\x20-\x7E]'), '');
}
```

```dart
removeNonASCII('äÄçÇéÉêlorem-ipsumöÖÐþúÚ'); // 'lorem-ipsum'
```
