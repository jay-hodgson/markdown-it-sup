# markdown-it-sup-alt

[![Build Status](https://img.shields.io/travis/jay-hodgson/markdown-it-sup/master.svg?style=flat)](https://travis-ci.org/jay-hodgson/markdown-it-sup)
[![NPM version](https://img.shields.io/npm/v/markdown-it-sup-alt.svg?style=flat)](https://www.npmjs.org/package/markdown-it-sup-alt)
[![Coverage Status](https://img.shields.io/coveralls/markdown-it/markdown-it-sup/master.svg?style=flat)](https://coveralls.io/r/jay-hodgson/markdown-it-sup?branch=master)

> Superscript (`<sup>`) tag plugin for [markdown-it](https://github.com/markdown-it/markdown-it) markdown parser.

__v1.+ requires `markdown-it` v4.+, see changelog.__

`29^th^` => `29<sup>th</sup>`

Markup is based on [pandoc](http://johnmacfarlane.net/pandoc/README.html#superscripts-and-subscripts) definition. But nested markup is currently not supported.

Forked from [upstream](https://github.com/markdown-it/markdown-it-sup) to allow unescaped whitespace within delimiters (still must be in the same line).
If using this plugin, it's recommended that you also use a math plugin so that text like 2^4 + 3^5 is handled properly.

## Install

node.js, browser:

```bash
npm install markdown-it-sup-alt --save
bower install markdown-it-sup-alt --save
```

## Use

```js
var md = require('markdown-it')()
            .use(require('markdown-it-sup-alt'));

md.render('29^th^') // => '<p>29<sup>th</sup></p>'
```

_Differences in browser._ If you load script directly into the page, without
package system, module will add itself globally as `window.markdownitSup`.


## License

[MIT](https://github.com/jay-hodgson/markdown-it-sup/blob/master/LICENSE)
