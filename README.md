# [type-mark](http://www.ejrbuss.net/type-mark)

## Why use type-mark

Because `typeof` just doesn't cut it. The canonical example being
```js
> typeof null
"object"
```
With type-mark checking for `null` is as easy as
```js
> type(null).object
false
```
Not to mention the added benifits of [modifiers](#modifiers), [interfaces](#interfaces), and
[custom validation](#writing-your-own-tests).

## Get It

### On the Client

You can use the rawgit CDN to get the latest minified version

```html
<script type="text/javascript" src="{{ site.cdn }}"></script>
```

Or you can include your own. Just save a copy of the minified file to your
site's javascript directory.

```html
<script type="text/javascript" src="js/type-mark.min.js"></script>
```

Using any of the above methods will make type-check available via your
choice of commonjs interface. If `require` is not defined type-check defines
`type` on the window. You can use `type.collision` to access any previous
value of `window.type`.

### On Node

type-mark is available through [npm](https://www.npmjs.com/). When using
[node.js](https://nodejs.org/en/) you can install using npm

```bash
$ npm install type-mark
```

In order to actually use type-mark in your Node project you will need to
require it in using
```js
var type = require('type-mark');
```

### From Scratch

You can also clone the git repository if you want the full source or are
interested in making modifications. type-check is dependency free so working
with it is as easy as cloning.

```bash
$ git clone https://github.com/ejrbuss/type-mark.git
```

To run the npm scripts you will need to run `npm install` as well as the
following global dependencies

- [mocha](https://mochajs.org/),
- [istanbul](https://istanbul.js.org/),
- [browserify](http://browserify.org/),
- [uglify-js](https://www.npmjs.com/package/uglify-js) and
- [jekyll/bundle](https://jekyllrb.com/).

The following npm scripts are made avaialble

```bash
$ npm run test     # run tests
$ npm run coverage # generate istanbul html report
$ npm run build    # build type-mark.js and type-mark.min.js for the client
$ npm run site     # run the docs site
```

## [Getting Started](http://www.ejrbuss.net/type-mark/#getting-started)