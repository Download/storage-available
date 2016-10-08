# storage-available
#### Detect if web storage is available and functional

[![npm](https://img.shields.io/npm/v/storage-available.svg)](https://npmjs.com/package/storage-available)
[![license](https://img.shields.io/npm/l/storage-available.svg)](https://opensource.org/licenses/MIT)

<sup><sub><sup><sub>.</sub></sup></sub></sup>

This microscopically small module contains only a single function, `storageAvailable`, that detects whether the Web Storage API methods are available. The reason you would want to use a separate module for feature detecting Web Storage is because it is [hard and error prone](https://gist.github.com/paulirish/5558557).

This function is the one [recommended](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API#Feature-detecting_localStorage) by the MDN documentation on Web Storage. I can claim copyright (and share it with you under the MIT license) because I [contributed](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API$compare?from=841355&to=909313) that part of the docs.


## Install

```sh
npm install --save storage-available
```

## Require

```js
var storageAvailable = require('storage-available')
```

## Import
```js
import storageAvailable from 'storage-available'
```

## Usage

```js
if (storageAvailable('localStorage')) {
  // Yippee! We can use localStorage awesomeness
}
else {
  // Too bad, no localStorage for us
}
```

You can test for sessionStorage instead by calling `storageAvailable('sessionStorage')`.

> **NOTE**: This module is intended for use in the browser, or other environments that natively support Web Storage. Use it via a web bundler such as Browserify or Webpack.

## Credits
Credits to [Paul Irish](https://gist.github.com/paulirish) for hist gist summarizing the development of feature detecting localStorage, and to all people who contributed fixes to it in that process.

## Issues
Add an issue in this project's [issue tracker](https://github.com/download/storage-available/issues)
to let me know of any problems you find, or questions you may have.

## Copyright
Copyright 2016 by [Stijn de Witt](http://StijnDeWitt.com). Some rights reserved.

## License
Licensed under the [MIT](https://opensource.org/licenses/MIT) Open Source license.

