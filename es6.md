# ES6

## Introduction

ECMAScript 6, also known as ECMAScript 2015, is the latest version of the ECMAScript standard. ES6 is a significant update to the language, and the first update to the language since ES5 was standardized in 2009.

## New Features

The new features specifically listed below are replacing features that used to be handled by internal tooling.

### Imports / Exports

Documentation:

- [Imports](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)
- [Exports](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export)

You should make use of named exports often.  By using named exports you make it much easier for the build tools to optimize the code as much as possible.

Since we now build with babel and webpack, you will need to be more strict in how you handle dynamic imports.

If you want to import a file that is known at compile time, then you can use `require`.  Webpack knows how to handle `require` statements, and babel will not complain about top level imports.

```js
export const func = () => {
  // Known at compile time
  return require('./something');
};
```

However, if your import is not known at compile time, then you will need to follow the instructions for [webpack dynamic requires](https://webpack.github.io/docs/context.html).

### Classes

Documentation: [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes).

ES6 classes are a simple sugar over the prototype-based OO pattern. Having a single convenient declarative form makes class patterns easier to use, and encourages interoperability. Classes support prototype-based inheritance, super calls, instance and static methods and constructors.

## Example Class File Structure

The following is an example of how to generally structure an es6 class file:

```js
// Standard library
import path from 'path';

// Externally developed node modules
import debug from 'debug';

// Internally developed node_modules
import View from 'timestep/ui/View';

// Project code
import PieModel from 'src/PieModel';


// Constants at the top
export const MY_CONST = 4;

// Then some private singletons
const log = debug('myGame:PieView');


// It is nice to leave double lines between conceptual blocks of code
// Export default should be the class, and the name of the class should match/
// the name of the file.
export default class PieView extends View {
  // Documentation doesnt have to be as verbose in es6
  /**
   * @param {Object} opts
   * @param {string} [opts.type='apple']
   **/
  constructor (opts = {}) {
    opts.type = opts.type || 'apple';
    opts.url = 'resources/images/' + opts.type;
    // Must call super before any references to `this`.
    super(opts);

    this._type = opts.type;
  }

  // You can easily create getters and setters now!
  get type () { return this._type; }
  set type (v) {
    log('new type:', v);
    this._type = v;
  }

  // Mark methods as private with an `_` prefix
  _privateMethod () {
    // do things
  }

  toString () {
    return `PieView(${this.type})`;
  }
}
```

## Resources

- [Full list of ES6 features](https://github.com/lukehoban/es6features)
- [MDN JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference);

### Examples

- [ledger-proposal example](https://github.com/jsio-private/ledger-proposal/tree/master/examples/everwing)
- [face-decorator editor UI](https://github.com/jsio-private/face-decorator/tree/master/editor-ui)
