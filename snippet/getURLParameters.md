---
title: getURLParameters
tags: Dart,string,uri,intermediate
---
Returns an String containing the parameters of the current URL or an empty String in case tehe parameter doesn´t contain parameters or is not a proper URI.

Use `String` concatanation and `Map<String, String> get queryParameters` to decode key and value from de url.

```dart
String getURLParameters (String url) {
  String str = '';
  Uri.parse(url).queryParameters.forEach((k, v) {
    str += ('$k: $v ');
  });
  return str;
}
```

```dart
getURLParameters('http://url.com/page?name=Alice&surname=Smith'); //name: Alice surname: Smith
print(getURLParameters('http://url.com/page?name=Alice&surname= ')); //name: Alice surname:  
print(getURLParameters('http://url.com')); //empty string
print(getURLParameters('not.url')); //empty string
```
