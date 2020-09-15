---
title: mask
tags: string,utility,intermediate
---

Replaces all but the last `num` runes of a string with the specified `mask`.

- Use `String.substring()` to grab the last `num` runes, `String.padLeft()` to fill the beginning of the string with the `mask` up to the original length.
- Omit the optional parameter, `num`, to keep a default of `4` runes unmasked.
- Omit the optional parameter, `mask`, to use the default of `'*'`.

```dart
String mask(String str, {int num = 4, String mask = '*'}) {
  return str.substring(str.length - num).padLeft(str.length, mask);
}
```

```dart
mask('1234567890'); // '******7890'
mask('1234567890', num: 3); // '*******890'
mask('1234567890', num: 4, mask: '\$'); // '$$$$$$7890'
```
