# Webpack Tutorial
An introduction to webpack using [their tutorial](http://webpack.github.io/docs/tutorials/getting-started/)

## What is Webpack?
Webpack is a build system that compiles your assets for your application. It follows a code over configuration methodology, unlike other build systems like grunt or gulp + browserify.

## Installation

If you have `Node` installed, type in the following command.

```
$ npm install webpack -g
```

## Compilation

In their CLI app, webpack takes two arguments. The main file and the compilation file. Here's a sample command.

```
$ webpack ./entry.js bundle.js
```

## Binding Loaders

Stealing this list of loaders from the [webpack-demos readme](https://raw.githubusercontent.com/ruanyf/webpack-demos/master/README.md):

1. Entry file - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo01-entry-file-source)
1. Multiple entry files - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo02-multiple-entry-files-source)
1. [Babel-loader](https://www.npmjs.com/package/babel-loader) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo03-babel-loader-source)
1. [CSS-loader](https://www.npmjs.com/package/css-loader), [Style-Loader](https://www.npmjs.com/package/style-loader) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo04-css-loader-source)
1. [Image loader](https://www.npmjs.com/package/url-loader) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo05-image-loader-source)
1. [CSS Module](https://github.com/css-modules/css-modules), [Demo with Webpack](https://css-modules.github.io/webpack-demo/) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo06-css-module-source)
1. [UglifyJs Plugin](http://webpack.github.io/docs/list-of-plugins.html#uglifyjsplugin) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo07-uglifyjs-plugin-source)
1. Environment flags - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo08-environment-flags-source)
1. Common chunk - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo09-common-chunk-source)
1. Vendor chunk - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo10-vendor-chunk-source)
1. [Exposing Global Variables](http://webpack.github.io/docs/library-and-externals.html) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo11-exposing-global-variables-source)
1. [React hot loader](http://gaearon.github.io/react-hot-loader/) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo12-react-hot-loader-source)
1. [React router](https://github.com/rackt/react-router/blob/0.13.x/docs/guides/overview.md) - [Webpack Demo](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo13-react-router-source)

### Babel-loader

This allows for ES6 features of the JS language to be utilized to the fullest before browser support. Things such as `import` are super useful instead of all of those `require` statements. Not to mention if you only want a portion of the export, like specific classes or functions, it becomes super useful. Think the import style of Python. 

### Environment Flags Example

```js
var devFlagPlugin = new webpack.DefinePlugin({
  __DEV__: JSON.stringify(JSON.parse(process.env.DEBUG || 'false'))
});
```

### Common Chunk Example

```js
var CommonsChunkPlugin = require("webpack/lib/optimize/CommonsChunkPlugin");
```

### Vendor Chunk Example

```js
module.exports = {
  entry: {
    app: './main.js',
    vendor: ['jquery'],
  },
  output: {
    filename: 'bundle.js'
  },
  plugins: [
    new webpack.optimize.CommonsChunkPlugin(/* chunkName= */'vendor', /* filename= */'vendor.js')
  ]
};
```

### React Hot Loader
For my current project, I'm using [React](http://facebook.github.io/react/). For React to work with Webpack, I need to make sure Hot is enabled for [Hot Module Replacement](http://webpack.github.io/docs/hot-module-replacement-with-webpack.html). Also, the [React Hot Loader](http://gaearon.github.io/react-hot-loader/) module must be installed as well.

## CLI

Some command-line options you should know. Again, credits to [Webpack Demos](https://github.com/ruanyf/webpack-demos/).

- `webpack` – for building once for development
- `webpack -p` – for building once for production (minification)
- `webpack --watch` – for continuous incremental build
- `webpack -d` – to include source maps
- `webpack --colors` – for making things pretty
* `webpack --progress` - Shows progress in the terminal output during compilation

## Resources

As I'm researching more about Webpack, I'm going to place my resources down here.

* [Webpack Docs](http://webpack.github.io/docs/)
* [Angular Webpack Example](https://github.com/jeffling/angular-webpack-example)
* [Webpack Demos](https://github.com/ruanyf/webpack-demos) - The ReadMe includes a good introduction to Webpack
* [Diving Webpack](https://web-design-weekly.com/2014/09/24/diving-webpack/) - Web Design Weekly's introduction to Webpack.
* [Webpack-HowTo](https://github.com/petehunt/webpack-howto) - Pete Hunt's guide to Webpack, which is fairly comprehensive for advanced features.
* [Christian Alfoni's Webpack Guide](http://www.christianalfoni.com/articles/2014_12_13_Webpack-and-react-is-awesome) Goes through Webpack features. I especailly like his examples on Handling Vendors
* [Corey House on Medium - Webpack vs. Browserify](https://medium.com/@housecor/browserify-vs-webpack-b3d7ca08a0a9)
* [Webpack Cookbook](https://github.com/gaearon/react-hot-loader/blob/master/docs/Troubleshooting.md) - Juho Vepsäläinen & Christian Alfoni's book on specific problems you may encounter in Webpack
* [SurviveJS Book](http://survivejs.com/webpack_react) - Juho Vepsäläinen's book on using React and Webpack together.
