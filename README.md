# html-tag [![NPM version](https://img.shields.io/npm/v/html-tag.svg?style=flat)](https://www.npmjs.com/package/html-tag) [![NPM monthly downloads](https://img.shields.io/npm/dm/html-tag.svg?style=flat)](https://npmjs.org/package/html-tag) [![NPM total downloads](https://img.shields.io/npm/dt/html-tag.svg?style=flat)](https://npmjs.org/package/html-tag) [![Linux Build Status](https://img.shields.io/travis/jonschlinkert/html-tag.svg?style=flat&label=Travis)](https://travis-ci.org/jonschlinkert/html-tag)

> Generate HTML elements from a javascript object.

Please consider following this project's author, [Jon Schlinkert](https://github.com/jonschlinkert), and consider starring the project to show your :heart: and support.

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

Force a tag to _not render_ the closing tag by passing boolean `false` as the last argument (this is sometimes necessary with XML implementations).

```js
console.log(tag('P', 'Some random text...', false));
//=> <P>Some random text...

console.log(tag('P', false));
//=> <P>
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

<details>
<summary><strong>Contributing</strong></summary>

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

</details>

<details>
<summary><strong>Running Tests</strong></summary>

Running and reviewing unit tests is a great way to get familiarized with a library and its API. You can install dependencies and run tests with the following command:

```sh
$ npm install && npm test
```

</details>

<details>
<summary><strong>Building docs</strong></summary>

_(This project's readme.md is generated by [verb](https://github.com/verbose/verb-generate-readme), please don't edit the readme directly. Any changes to the readme must be made in the [.verb.md](.verb.md) readme template.)_

To generate the readme, run the following command:

```sh
$ npm install -g verbose/verb#dev verb-generate-readme && verb
```

</details>

### Related projects

You might also be interested in these projects:

* [breakdance](https://www.npmjs.com/package/breakdance): Breakdance is a node.js library for converting HTML to markdown. Highly pluggable, flexible and easy… [more](http://breakdance.io) | [homepage](http://breakdance.io "Breakdance is a node.js library for converting HTML to markdown. Highly pluggable, flexible and easy to use. It's time for your markup to get down.")
* [html-toc](https://www.npmjs.com/package/html-toc): Generate a HTML table of contents using cheerio. | [homepage](https://github.com/jonschlinkert/html-toc "Generate a HTML table of contents using cheerio.")
* [is-self-closing](https://www.npmjs.com/package/is-self-closing): Returns true if the given name is a HTML void element or common SVG self-closing… [more](https://github.com/jonschlinkert/is-self-closing) | [homepage](https://github.com/jonschlinkert/is-self-closing "Returns true if the given name is a HTML void element or common SVG self-closing element.")
* [remarkable](https://www.npmjs.com/package/remarkable): Markdown parser, done right. 100% Commonmark support, extensions, syntax plugins, high speed - all in… [more](https://github.com/jonschlinkert/remarkable) | [homepage](https://github.com/jonschlinkert/remarkable "Markdown parser, done right. 100% Commonmark support, extensions, syntax plugins, high speed - all in one.")
* [self-closing-tags](https://www.npmjs.com/package/self-closing-tags): HTML void elements are not the only self-closing tags. This includes common SVG self-closing elements… [more](https://github.com/jonschlinkert/self-closing-tags) | [homepage](https://github.com/jonschlinkert/self-closing-tags "HTML void elements are not the only self-closing tags. This includes common SVG self-closing elements as well.")

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](https://twitter.com/jonschlinkert)

### License

Copyright © 2017, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT License](LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.6.0, on November 01, 2017._