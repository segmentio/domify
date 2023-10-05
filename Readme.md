# domify

> **Note**  
> Segment has paused maintenance on this project, but may return it to an active status in the future. Issues and pull requests from external contributors are not being considered, although internal contributions may appear from time to time. The project remains available under its open source license for anyone to use.

Turn HTML into DOM elements x-browser.

## Usage

Works out of the box in the browser:

```js
var domify = require('domify');

document.addEventListener('DOMContentLoaded', function() {
  var el = domify('<p>Hello <em>there</em></p>');
  document.body.appendChild(el);
});
```

You can also run it in *node* and *iojs*. Just pass a custom implementation of `document`:

```js
var jsdom = require('jsdom').jsdom();

domify('<p>Hello <em>there</em></p>', jsdom.defaultView.document);
```

## Running tests

```
$ npm i -g component-test
$ make
$ component-test browser
```

## License

MIT
