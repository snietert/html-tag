# html-tag [![NPM version](https://img.shields.io/npm/v/html-tag.svg?style=flat)](https://www.npmjs.com/package/html-tag) [![NPM monthly downloads](https://img.shields.io/npm/dm/html-tag.svg?style=flat)](https://npmjs.org/package/html-tag)  [![NPM total downloads](https://img.shields.io/npm/dt/html-tag.svg?style=flat)](https://npmjs.org/package/html-tag) [![Linux Build Status](https://img.shields.io/travis/jonschlinkert/html-tag.svg?style=flat&label=Travis)](https://travis-ci.org/jonschlinkert/html-tag)

> Generate HTML elements from a javascript object.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save html-tag
```

Originally inspired by an HTML helper in hexo by [Tommy Chen](https://github.com/tommy351).

## Usage

```js
var tag = require('html-tag');
tag(name[, attribs, text]);
```

**Params**

* `tag` **{String}**: Name of the tag to create.
* `attribs` **{Object}**: Optional attributes
* `text` **{String|Boolean}**: Optional text
* `returns` **{String}**: string of HTML

**Examples**

```js
console.log(tag('a', {href: 'https://sellside.com'}, 'Sellside'));
//=> <a href="https://sellside.com">Sellside</a>

console.log(tag('a', {id: 'anchor'}));
//=> <a id="anchor"></a>

console.log(tag('strong', 'Let\'s dance!'));
//=> <strong>Let's dance</strong>

console.log(tag('div'));
//=> <div></div>
```

**Void elements (self-closing tags)**

```js
console.log(tag('img', {src: 'foo.jpg'}));
//=> <img src="foo.jpg">

console.log(tag('br'));
//=> <br>

console.log(tag('br', '\nfoo'));
//=> <br>\nfoo
```

**Boolean attributes**

Boolean attributes are defined by defining the attribute with a boolean value (strictly `true` or strictly `false`)

```js
console.log(tag('details', {open: true}));
//=> <details open></details>

console.log(tag('details', {open: false}));
//=> <details></details>

console.log(tag('details', {open: 'false'}));
//=> <details open="false"></details>
```

## About

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Building docs

_(This document was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme) (a [verb](https://github.com/verbose/verb) generator), please don't edit the readme directly. Any changes to the readme must be made in [.verb.md](.verb.md).)_

To generate the readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install -g verb verb-generate-readme && verb
```

### Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

### License

Copyright © 2017, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.3.0, on January 08, 2017._