# hast-util-sectioning [![Build Status][build-badge]][build-page] [![Coverage Status][coverage-badge]][coverage-page]

Check if a [node][] is a [**sectioning**][spec] [element][].

## Installation

[npm][]:

```bash
npm install hast-util-sectioning
```

## Usage

```javascript
var sectioning = require('hast-util-sectioning');

sectioning({
  type: 'element',
  tagName: 'a',
  properties: {href: '#alpha', title: 'Bravo'},
  children: [{type: 'text', value: 'Charlie'}]
}); //=> false

sectioning({
  type: 'element',
  tagName: 'article',
  children: [{
    type: 'element',
    tagName: 'p',
    children: [{type: 'text', value: 'Delta'}]
  }]
}); //=> true
```

## API

### `sectioning(node)`

Check if the given value is a [**sectioning**][spec] [element][].

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definition -->

[build-badge]: https://img.shields.io/travis/wooorm/hast-util-sectioning.svg

[build-page]: https://travis-ci.org/wooorm/hast-util-sectioning

[coverage-badge]: https://img.shields.io/codecov/c/github/wooorm/hast-util-sectioning.svg

[coverage-page]: https://codecov.io/github/wooorm/hast-util-sectioning?branch=master

[npm]: https://docs.npmjs.com/cli/install

[license]: LICENSE

[author]: http://wooorm.com

[node]: https://github.com/wooorm/hast#node

[element]: https://github.com/wooorm/hast#element

[spec]: https://html.spec.whatwg.org/#sectioning-content