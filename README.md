# lint-templates [![NPM version](https://badge.fury.io/js/lint-templates.svg)](http://badge.fury.io/js/lint-templates)

> Finds helpers that aren't registered and variabled that aren't defined on the context. Can be used as a middleware with assemble, Template, verb, generate, and other apps built on Template.

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i lint-templates --save
```

## Usage

```js
var lint = require('lint-templates');
```

**Middleware**

Use as a middleware with [Template] or Template-based applications, like [assemble], [verb], or [generate].

```js
var lint = require('lint-templates');

module.exports = function (app) {
  return function(file, next) {
    lint(app, file);
    next();
  };
};
```

Register the middleware:

```js
template.onLoad(/\.hbs/, lint(app));
```

Any of the following middleware VERBs should work:

* `.onLoad`
* `.preRender`
* `.preCompile`
* `.use`
* `.all`

Any of these "stages" might give you useful information depending how your project is setup.

## Related projects

<!-- add an array of related projects, then un-escape the helper -->

* [assemble](http://assemble.io): Static site generator for Grunt.js, Yeoman and Node.js. Used by Zurb Foundation, Zurb Ink, H5BP/Effeckt,… [more](http://assemble.io)
* [rethrow](https://github.com/jonschlinkert/rethrow): Re-throw an error to get better error reporting for templates.
* [template](https://github.com/jonschlinkert/template): Render templates using any engine. Supports, layouts, pages, partials and custom template types. Use template… [more](https://github.com/jonschlinkert/template)
* [verb](https://github.com/assemble/verb): Documentation generator for GitHub projects. Extremely powerful, easy to use, can generate anything from API… [more](https://github.com/assemble/verb)

## Running tests

Install dev dependencies:

```sh
$ npm i -d && npm test
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/lint-templates/issues/new)

## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2015 Jon Schlinkert
Released under the MIT license.

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on May 24, 2015._