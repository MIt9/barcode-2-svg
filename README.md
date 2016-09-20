# barcode-2-svg

Create svg file on server side without canvas
it's modificated version of [JQUERY PLUGIN : BARCODE](http://barcode-coder.com/en/barcode-jquery-plugin-201.html)
Generate 1D and 2D barcodes

## Supported 1D types

* [Code39](http://en.wikipedia.org/wiki/Code39)
* [Codabar](http://en.wikipedia.org/wiki/Codabar)
* [Code128](http://en.wikipedia.org/wiki/Code128)
* [UPC-A](http://en.wikipedia.org/wiki/Universal_Product_Code)
* [UPC-E](http://en.wikipedia.org/wiki/Universal_Product_Code#UPC-E)
* [EAN-13](http://en.wikipedia.org/wiki/EAN)


## Supported 2D types

* [QR Code](http://en.wikipedia.org/wiki/QR_Code) (comming soon)
* [DataMatrix](http://en.wikipedia.org/wiki/DataMatrix) (comming soon)
* [PDF417](http://en.wikipedia.org/wiki/PDF417) (comming soon)

## Requirements

- A working installation of [GraphicsMagick](http://www.graphicsmagick.org/).
- node >= 0.10.0

## Installing

	npm install barcode

## Usage

Set it up and specify your type and options. The following 3 are the only
required ones.

```javascript
var barcode = require('barcode-2-svg');
var code39 = barcode("9234567890128", "ean13",
{width:'50', barWidth:1, barHeight:50});
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

 - barHeight (int) -height of svg (default: 30);
 - width (int) -width of svg (default: 100);
 - bgColor (text) -background color (default: '#FFFFFF');
 - color (text) -barcode color (default: '#000000');


----------


## License

[The MIT License (MIT)](http://opensource.org/licenses/mit-license.php)