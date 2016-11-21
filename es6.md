# ES6

## Introduction

ECMAScript 6, also known as ECMAScript 2015, is the latest version of the ECMAScript standard. ES6 is a significant update to the language, and the first update to the language since ES5 was standardized in 2009.

## Imports

You should organize imports in to logical blocks, based on where they are coming from.  For example:

``` js
// Standard library
import path from 'path';

// Externally developed node modules
import debug from 'debug';

// Internally developed node_modules
import timestep from 'timestep';

// Project code
import GameView from 'src/GameView';
```

## Classes

ES6 classes are a simple sugar over the prototype-based OO pattern. Having a single convenient declarative form makes class patterns easier to use, and encourages interoperability. Classes support prototype-based inheritance, super calls, instance and static methods and constructors.

```js
import Food from 'food';

// Class that extends an existing class
class Cake extends Food {

  // constructor with arguments
  constructor (protein, carbs, fat) {
    // call super constructor
    super("Cake", protein, carbs, fat);
  }

  toString () {
    return this.name;
  }
}
```

## Resources

[Full list of ES6 features](https://github.com/lukehoban/es6features)
