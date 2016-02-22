# space-separated-tokens [![Build Status][build-badge]][build-page] [![Coverage Status][coverage-badge]][coverage-page]

Parse and stringify space-separated tokens according to the [spec][].

## Installation

[npm][]:

```bash
npm install space-separated-tokens
```

**space-separated-tokens** is also available as an AMD, CommonJS, and
globals module, [uncompressed and compressed][releases].

## Usage

Dependencies:

```javascript
var spaceSeparated = require('space-separated-tokens');
```

Parsing:

```javascript
var values = spaceSeparated.parse(' foo\tbar\nbaz  ');
```

Yields:

```js
[ 'foo', 'bar', 'baz' ]
```

Compiling:

```javascript
var value = spaceSeparated.stringify(values);
```

Yields:

```js
'foo bar baz'
```

## API

### `spaceSeparated.parse(value)`

Parse space-separated tokens to an array of strings, according to the [spec][].

*   `value` (`string`) — space-separated tokens.

**Returns**: `Array.<string>` — List of tokens.

### `spaceSeparated.stringify(values)`

Compile an array of strings to space-separated tokens.
Note that it’s not possible to specify empty or white-space only values.

*   `values` (`Array.<string>`) — List of tokens.

**Returns**: `string` — Space-separated tokens.

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definition -->

[build-badge]: https://img.shields.io/travis/wooorm/space-separated-tokens.svg

[build-page]: https://travis-ci.org/wooorm/space-separated-tokens

[coverage-badge]: https://img.shields.io/codecov/c/github/wooorm/space-separated-tokens.svg

[coverage-page]: https://codecov.io/github/wooorm/space-separated-tokens?branch=master

[npm]: https://docs.npmjs.com/cli/install

[releases]: https://github.com/wooorm/space-separated-tokens/releases

[license]: LICENSE

[author]: http://wooorm.com

[spec]: https://html.spec.whatwg.org/#space-separated-tokens
