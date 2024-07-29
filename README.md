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
- [css-color-names](https://www.npmjs.com/package/css-color-names) doesn't have RGB values.
- [html-colors](https://www.npmjs.com/package/html-colors) doesn't have RGB values.
- [css-spec-colors](https://www.npmjs.com/package/css-spec-colors) returns RGB values in the form of a CSS `rgb()` string.
- [named-css-colors](https://www.npmjs.com/package/named-css-colors) looks like a great package and it existed before this package (full disclosure: I did not know this beforehand). However, in contrast to this package: it calculates RGB values from hex, freezes objects, and includes some extra utils. If RGB values are all you need, and you want the most lightweight and performant option, you should use `css-color-names-rgb` instead.



# Contributing
## Publishing
```sh
npm version <whatever>
npm publish
git push --follow-tags
```
