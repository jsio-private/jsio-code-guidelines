# jsio-webpack

## Usage

### `package.json`

This is an example of what your `package.json` should contain (in relation to jsio-webpack):

```json
{
  "scripts": {
    "build": "NODE_ENV=production jsio-webpack", // NODE_ENV=production is required for production builds!
    "watch": "jsio-webpack --watch",
    "serve": "jsio-webpack serve --hot"
  },
  "devDependencies": {
    "jsio-webpack": "git+https://github.com/jsio-private/jsio-webpack"
  }
}
```

### Coding debug features

When coding debug features, you should check if `process.env.NODE_ENV` is set to development or production:

```js
if (process.env.NODE_ENV === 'development') { // Can also be production
  console.log("run debug features");
}
```

### `jsio-webpack.config.js`

This is very similar to a standard `webpack.config.js`, except you do not need to worry about configuring loaders or plugins (unless you want to).

You must either export a configure function, or an object:

- `{function} configure`
- `{function} [postConfigure]`


```js
'use strict';
const path = require('path');

const configure = (configurator, options) => {
  // Add your project specific config!
  configurator.merge({
    entry: {
      test: path.resolve(__dirname, 'testIndex.js')
    },
    output: {
      filename: '[name].js',
      path: path.resolve(__dirname, 'dist'),
      publicPath: '/'
    }
  });

  // Set options for the jsio-webpack config generators
  options.useStylusExtractText = true;

  return configurator;
};


const postConfigure = (configurator, options) => {
  // If you want to remove a plugin provided by jsio-webpack
  configurator.removePreLoader('eslint');
};

module.exports = {
  configure: configure,
  postConfigure: postConfigure
};
```

## Resources

- [Git repository](https://github.com/jsio-private/jsio-webpack/blob/master/readme.md)

### Example projects

- [ledger-proposal example](https://github.com/jsio-private/ledger-proposal/tree/master)
- [face-decorator editor UI](https://github.com/jsio-private/face-decorator/tree/master)
