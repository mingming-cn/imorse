# IMorse

> **IMorse** is a pure javascript(~1.5kb) library for encoding / decoding morse code messages, **unicode supported**.

[中文说明文档](README_ZH.md) | [Online DEMO 地址](https://toolb.cn/morse) 

[![Build Status](https://github.com/mingming-cn/imorse/workflows/build/badge.svg)](https://github.com/mingming-cn/imorse/actions)
[![Coverage Status](https://coveralls.io/repos/github/mingming-cn/imorse/badge.svg?branch=master)](https://coveralls.io/github/mingming-cn/imorse?branch=master)
[![npm](https://img.shields.io/npm/v/imorse.svg)](https://www.npmjs.com/package/imorse)
[![npm](https://img.shields.io/npm/dm/imorse.svg)](https://www.npmjs.com/package/imorse)
[![npm](https://img.shields.io/npm/l/imorse.svg)](https://www.npmjs.com/package/imorse)


# 1. Install

> **npm install imorse**

Or download `dist/imorse.min.js` source file。

# 2. Import It

 - `Script` tag.

```html
<script type="text/javascript" src="dist/imorse.min.js"></script>
```

 - `ES6` style.

```ts
import { decode, encode } from 'imorse';
```


# 3. Usage & API

There is only 2 API named `encode`, `decode`. For `encode(msg, [option])`, example:

```ts
import { decode, encode } from 'imorse';
// standart morse
encode('Hello, IMorse!');
  
// unicode
encode('コンニチハ, セカイ!');
encode('越过长城，走向世界');

// option
const option = {
  space: ' ',
  long: '-',
  short: '*'
};
encode('越过长城，走向世界', option);
```

For `decode(morse, [option])`, example:

```ts
import { decode, encode } from 'imorse';
decode('../.-../---/...-/./-.--/---/..-/-/---/---/--...-....-...-/-..---..-.-----/---..-...--...-/-..----.--.....');

// option
const option = {
  space: ' ',
  long: '-',
  short: '*'
};
decode('*-** --- ***- *', option);
```


# 4. Test

```bash
$npm install

$npm test
```


# 5. LICENSE

Fork MIT@[hustcc](https://github.com/hustcc)
