[![npm version](https://img.shields.io/npm/v/css-color-names-rgb.svg)](https://www.npmjs.com/package/css-color-names-rgb)
[![Downloads](https://img.shields.io/npm/dm/css-color-names-rgb.svg)](https://www.npmjs.com/package/css-color-names-rgb)
![Uses TypeScript](https://img.shields.io/badge/Uses-Typescript-294E80.svg)


# css-color-names-rgb

These are the CSS color names from [the CSS spec](https://drafts.csswg.org/css-color/#named-colors), as numeric RGB values.

Does not include `transparent` or `currentcolor`.

All color names are lowercase. If needed, transform colors using `myColor.toLowerCase()` before passing.

This library is optimized for parsing using `JSON.parse` (See https://v8.dev/blog/cost-of-javascript-2019#json).


## Example

```ts
import { cssColors } from 'css-color-names-rgb';

console.log(cssColors.papayawhip);
// [255, 239, 213]
```


## Utilities

```ts
import {
  type ColorName,
  isCssColorName,
  getColor,
} from 'css-color-names-rgb';
```


## Comparison with other libraries
- [color-name](https://github.com/colorjs/color-name) doesn't have types included (DT only), and doesn't use `JSON.parse` to optimize load time.
- [css-color-names](https://www.npmjs.com/package/css-color-names) doesn't have RGB values.
- [html-colors](https://www.npmjs.com/package/html-colors) doesn't have RGB values.
- [css-spec-colors](https://www.npmjs.com/package/css-spec-colors) returns RGB values in the form of a CSS `rgb()` string.
- [named-css-colors](https://www.npmjs.com/package/named-css-colors) calculates RGB values from hex, freezes objects, and includes extra utils.
