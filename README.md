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

1. [Entry file](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo01-entry-file-source)
1. [Multiple entry files](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo02-multiple-entry-files-source)
1. [Babel-loader](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo03-babel-loader-source)
1. [CSS-loader](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo04-css-loader-source)
1. [Image loader](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo05-image-loader-source)
1. [CSS Module](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo06-css-module-source)
1. [UglifyJs Plugin](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo07-uglifyjs-plugin-source)
1. [Environment flags](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo08-environment-flags-source)
1. [Common chunk](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo09-common-chunk-source)
1. [Vendor chunk](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo10-vendor-chunk-source)
1. [Exposing Global Variables](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo11-exposing-global-variables-source)
1. [React hot loader](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo12-react-hot-loader-source)
1. [React router](https://github.com/ruanyf/webpack-demos/blob/master/README.md#demo13-react-router-source)

###

### React Hot Loader
For my current project, I'm using [React](http://facebook.github.io/react/). For React to work with Webpack, I need to make sure Hot is enabled for [Hot Module Replacement](http://webpack.github.io/docs/hot-module-replacement-with-webpack.html). Also, the [React Hot Loader](http://gaearon.github.io/react-hot-loader/) module must be installed as well.

## CLI

* `--progress` - Shows progress in the terminal output during compilation
* `--colors` - Shows compilation in a beautiful color output

## Resources

As I'm researching more about Webpack, I'm going to place my resources down here.

* [Webpack Docs](http://webpack.github.io/docs/)
* [Angular Webpack Example](https://github.com/jeffling/angular-webpack-example)
* [Webpack Demos](https://github.com/ruanyf/webpack-demos) - The ReadMe includes a good introduction to Webpack
