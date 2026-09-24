# barcode-2-svg

> **Server-side barcode to SVG without canvas** — generate 1D barcodes (Code39, Code128, EAN-13, etc.) as SVG strings or files, no canvas required. Works in Node and modern browsers.

[![npm](https://img.shields.io/npm/v/barcode-2-svg.svg)](https://www.npmjs.com/package/barcode-2-svg)
[![node](https://img.shields.io/node/v/barcode-2-svg.svg)](https://nodejs.org)
[![license](https://img.shields.io/npm/l/barcode-2-svg.svg)](LICENSE)

Create svg file on server/browser side without canvas
Work well in all modern browser
it's modificated version of [JQUERY PLUGIN : BARCODE](http://barcode-coder.com/en/barcode-jquery-plugin-201.html)
Generate 1D barcodes

## Supported types

* [Code39](http://en.wikipedia.org/wiki/Code39)
* [Codabar](http://en.wikipedia.org/wiki/Codabar)
* [Code128](http://en.wikipedia.org/wiki/Code128)
* [EAN-13](http://en.wikipedia.org/wiki/EAN)

## Requirements

- Node >= 18
- Modern browsers (no IE)

## Install

```bash
npm install barcode-2-svg
# or
yarn add barcode-2-svg
```

## Quick Start

```javascript
import barcode from 'barcode-2-svg';

// SVG string (server or browser)
const svg = barcode("9234567890128", "ean13", {width: 200, barWidth: 2, barHeight: 80});
console.log(svg); // <svg>...</svg>

// Write to file (Node only)
barcode("9234567890128", "code39", {width: 200, barWidth: 2, barHeight: 80, toFile: true});
```

## Usage

Set it up and specify your type and options. The following 3 are the only
required ones.

```javascript
var barcode = require('barcode-2-svg');
//to file work only on server side
var code39 = barcode("9234567890128", "code39", {width:50, barWidth:1, barHeight:50, toFile:true});
//return barcode like text
var code13Text = barcode("9234567890128", "ean13", {width:50, barWidth:1, barHeight:50});
console.log(code13Text);
```
type (string)

- codabar
- code11 (code 11)
- code39 (code 39)
- code93 (code 93)
- code128 (code 128)
- ean8 (ean 8)
- ean13 (ean 13)
- std25 (standard 2 of 5 - industrial 2 of 5)
- int25 (interleaved 2 of 5)

settings (object):
 - toFile (bool) -write to file (default: false);
 - barHeight (int) -height of svg (default: 30);
 - width (int) -width of svg (default: 100);
 - bgColor (text) -background color css like (default: 'transparent');
 - color (text) -barcode color (default: '#000000');


----------


## License

[The MIT License (MIT)](http://opensource.org/licenses/mit-license.php)