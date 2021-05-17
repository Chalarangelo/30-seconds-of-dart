---
title: unescapeUnicode
tags: string,intermediate
---

Unescape the escape literals.

- Use `String.indexOf()` to find the first occurence of pattern, using a pattern(String).
- Use `String.substring()` to get the substring from the given range. here unicode characters.
- Use `int.parse()` to get the radix:16 int from string.
- Use `String.fromCharCode`returns string from charCode (UTF-16 code units).
- Used to unescape literals(unicodes here) from server side or processed literals that is usually escaped.
- Can be extended for showing different language characters too.
- Example, Used to parse emojis.

```dart
String unescapeUnicode(String content) {
  String regex = "\\u";
  int offset = content.indexOf(regex) + regex.length;
  while(offset > 1){
    int limit = offset + 4;
    String str = content.substring(offset, limit);
    if(str!=null && str.isNotEmpty){
      String uni = String.fromCharCode(int.parse(str,radix:16));
      content = content.replaceFirst(regex+str,uni);      
    }
    offset = content.indexOf(regex) + regex.length;
  }
  return content;
  
}
```

```dart
unescapeUnicode('\ud83d\ude0e Be Safe at your home') //😎 Be Safe at your home
```
