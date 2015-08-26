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

## React Hot Loader
For my current project, I'm using [React](http://facebook.github.io/react/). For React to work with Webpack, I need to make sure Hot is enabled for [Hot Module Replacement](http://webpack.github.io/docs/hot-module-replacement-with-webpack.html). Also, the [React Hot Loader](http://gaearon.github.io/react-hot-loader/) module must be installed as well.


