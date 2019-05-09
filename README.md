# Babel Root Import
Babel plugin to change the behaviour of `import` to root based paths.<br>

## Example
```javascript
// Usually
import SomeExample from '../../../some/example.js'

// With babel-root-slash-import
import SomeExample from '/some/example.js'
```

## Install
```
npm install --save-dev @share911/babel-plugin-root-slash-import
```

```
yarn add --dev @share911/babel-plugin-root-slash-import
```

## Use
Add a `.babelrc` file and write:
```javascript
{
  "plugins": [
    "@share911/babel-plugin-root-slash-import"
  ]
}
```
or pass the plugin with the plugins-flag on CLI
```
npx babel-node myfile.js --plugins @share911/babel-plugin-root-slash-import
```

## Extras
If you want a custom root because for example all your files are in the src/js folder you can define this in your `.babelrc` file
```javascript
{
  "plugins": [
    ["@share911/babel-plugin-root-slash-import", {
      "rootPathSuffix": "src/js"
    }]
  ]
}
```
