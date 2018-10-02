
## Quick start

All you need to use it, is only:

1) install package

```sh
npm install fast-react-render
```

2) replace you render to:

```js
var ReactRender = require('fast-react-render');

var element = React.createElement(Component, {property: 'value'});
console.log(ReactRender.elementToString(element, {context: {}}));
```

## Cache

React server rendering support cache for component.

First of all, you must choose cache system. It can be any system, which implement ICache interface ([interface](src/interfaces/i-cache.js)).
For caching, component must implement ICacheableComponent interface ([interface](src/interfaces/i-cacheable-component.js)).

Example with using LRU cache: [render with LRU cache](examples/cache.js) (install `lru-cache` package first).

## What's next

If you need more performance, you can try use [fast-react-server](https://github.com/alt-j/fast-react-server) - is high speed mock for react, which provide rendering **11 times as fast** as traditional, but require more configuration for build system.
