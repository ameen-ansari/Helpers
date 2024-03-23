## Javascript Best Practices Git Repo
```
https://github.com/airbnb/javascript
```

## Broken Emoji Remover
Use this in case of objects string `Recommended`
```
function removeBrokenEmoji(str) {
  return str.replace(
    /[\uD800-\uDBFF](?![\uDC00-\uDFFF])|(?<![\uD800-\uDBFF])[\uDC00-\uDFFF]|[\uFFFD]/g,
    '',
  );
}
```
Use this in case of input value change mean while when you handle a string
```
function removeSpecialCharacter(inputString) {
  return inputString.split('�').join('');
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

## Slice a String with Emoji
```
function sliceStringWithEmojis(str = '', start, end) {
  const sliced = Array.from(str).slice(start, end);
  return sliced.join('');
}
```
