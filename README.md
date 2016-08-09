# An SVG path reversal library

This is a simple SVG path reversal library, with a terribly simple API.

## installation

Install with npm:

```
$> npm install svg-path-reverse
```

## Using the library

This is a universal library, you can load it through require.js, UMD, commonjs, browser, whatever, it doesn't care. You probably know how to use the technology you've chosen to use. Once you've loaded it in, however that might be, the API is as follows:

```
var utils = ... // load however you know to load libraries
var reverse = utils.reverse,
    normalize = utils.normalize;

var path ="m0 0l10 0 0 10 -10 0z";

var normalized = normalize(path);
var reversed = reverse(path);
var reversed2 = reverse(reversed);

console.log("reversing is idempotent:", normalized === reversed2);

```

## LICENSE

This code is in the public domain, except in jurisdictions that do not recognise the public domain, where this code is MIT licensed.

## demo?

live demo (sort of): https://pomax.github.io/svg-path-reverse
