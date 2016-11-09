# React JS

This is a general outline of how to build react projects for js.io.



## Project Structure

React projects should be organized by component.  The top level should only contain support (config, readme) files and directories.  No implementation files should be at top level.

```
src/
| mask/
| | actions.js      # All actions that this component is responsible for
| | Mask.js         # The main component
| | Mask.styl       # All styles for this component
| | reducers.js     # All reducers that this component is responsible for
| |
| misc/             # All components which are purely display
| | Panel.js
| | Panel.styl
| | AbsOverlay.js
| | AbsOverlay.styl
| |
| app.js            # Entrypoint for the app
| App.styl          # Global styles (things like `html`, `body`)
|
.gitignore          # Support files and configuration at top level
package.json
readme.md
webpack.config.js
```



## CSS

All projects should make use of [stylus](https://github.com/stylus/stylus), with [nib](https://github.com/tj/nib) for browser prefixing.

All styles should be hyphenated: `my-style`.

All components top level node should be postfixed with `-cmpt` (if the component has any styles, or its children have any styles).  For example:

``` js
export default function AbsOverlay () {
  return (
    <div className='abs-overlay-cmpt' />
  );
};
```

``` css
.abs-overlay-cmpt
  background rgba(0, 0, 0, 0.2)
```



## JS

All js code should be written as es6 modules.  Babel should be used to build code with at least the `es2015` and `react` presets enabled.

``` js
query: { presets: ['es2015', 'react'] }
```

### Redux

React projects should use [react-redux](https://github.com/reactjs/react-redux).  Actions should be in `actions.js` and reducers should be in `reducers.js`.

Be sure to make use of `react-redux`'s `connect` function to keep your component implementation clean.

``` js
const mapStateToProps = state => {
  return {
    file: state.mask.file
  };
};

const mapDispatchToProps = dispatch => {
  return {
    setInputFile: file => dispatch(maskSetInputFile(file))
  };
};

export default connect(mapStateToProps, mapDispatchToProps)(Mask);
```


### Linting

All projects should make use of the following modules:

- eslint
- eslint-config-jsio
- eslint-plugin-promise
- eslint-plugin-react
- eslint-plugin-standard

Your `package.json` should be sure to properly configure `eslint`:

``` json
"eslintConfig": {
  "extends": [
    "jsio",
    "plugin:react/recommended"
  ],
  "plugins": [
    "react"
  ],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    }
  }
}
```

The project should also make use of `eslint-loader` in `webpack.config.js` to ensure the project always remains linted:

``` js
{ test: /\.js$/, loader: 'eslint-loader', exclude: /node_modules/ }
```



## Building

All projects should have the following entries in their package's `scripts`:

- `clean` Remove any built files
- `build` Build project for production deployment
- `watch` Build project for development, rebuild any time there is a change
- `lint` Run eslint on project


### `dist/`

It is common to include a `dist` directory, with built library files.  If a project has a `dist` directory, it should be excluded from normal commits.

The project should have at least two branches:

- `develop` No dist commits
- `master` Merges from develop, and dist commits

The last step of creating a pull request to master should be (roughly):

- `npm run build`
- `git add dist`
- `git commit -m "update dist"`
