identicon.js
=========

HTML5 based identicon library based on Jquery. 

Code is originally based on [Jquery Identicon5 Library](http://francisshanahan.com/identicon5/test.html) All Credits goes to the Author

Changes from Original
==================

* Renders directly into the `img` tag instead of creating a new canvas inside `li` tags
* Leverages data-* attributes in HTML5
* Leverages [DataURI](http://en.wikipedia.org/wiki/Data_URI_scheme#Web_browser_support) of the `img` and `canvas` to render the identicon within the `img` tag directly

Examples In New Version
=====================

HTML Source  looks like this.
```
<h1>Default Size Demo</h1>
<img data-md5="67905b29aaee2bc1fee59f8576d25ea3" class="identicon-1">
<img data-md5="77905b29aaee2bc1fee59f8576d25ea3" class="identicon-1">

<h1>Custom Size Demo</h1>
<img data-md5="87905b29aaee2bc1fee59f8576d25ea3" class="identicon-2">
<img data-md5="97905b29aaee2bc1fee59f8576d25ea3" class="identicon-2">
```
Javascript code looks like this
```
// Default identicons with size 32x32
$('img.identicon-1').identicon5({dataattr : 'md5'});
```
```
// identicons with size 128x128
$('img.identicon-2').identicon5({size : 128, dataattr : 'md5'});
```

Options
=======
1. `size` : size of the image in pixels.
2. `rotate` : true if the image should be rotated. (default: `true`)
3. `dataattr` : data-* attribute that should be used for finding the checksum (default: `md5`, i.e `data-md5` value will be looked up)

License
======
MIT
