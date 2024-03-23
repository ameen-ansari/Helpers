## Javascript Best Practices Git Repo
```
https://github.com/airbnb/javascript
```

## Broken Emoji Remover
```
function removeBrokenEmoji(str) {
  return str.replace(
    /[\uD800-\uDBFF](?![\uDC00-\uDFFF])|(?<![\uD800-\uDBFF])[\uDC00-\uDFFF]|[\uFFFD]/g,
    '',
  );
}
```

## Correct Length Counter Of a String [resolve emoji counter issue]
```
function strLengthCounter(str: string) {
  let count: number = 0;
  let arr: string[] = [...str];

  for (let c = 0; c < arr.length; c++) {
    if (
      arr[c] !== '\u{200D}' &&
      arr[c + 1] !== '\u{200D}' &&
      arr[c + 1] !== '\u{fe0f}' &&
      arr[c + 1] !== '\u{20e3}'
    ) {
      count++;
    }
  }
  return count;
}
```

## Remove Special Char From a Str
```
function removeSpecialCharacter(inputString) {
  return inputString.split('�').join('');
}
```

## Slice a String with Emoji
```
function sliceStringWithEmojis(str = '', start, end) {
  const sliced = Array.from(str).slice(start, end);
  return sliced.join('');
}
```
