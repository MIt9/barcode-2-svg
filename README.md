# barcode-2-svg

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

- node >= 0.10.0
- browser != IE

## Installing

	npm install barcode-2-svg

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