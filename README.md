# Node - Babel - ESNext 
Deomnstrate the usage patterns of transpiler (Babel) for a node project.

Setup for development cycle of a node module, including setup for transpilation of ES2015 features, and perhaps some experimental feature of ES7, including module loading, testing and editor setup (Sublime).

## Usage

  gulp test
  gulp watch
  # or
  npm test
  npm run watch


## Setup

- Start using `redux-voting-server` example
- Also look at: https://github.com/elierotenberg/es6-starterkit

## TODO

- Setup (package.son)
- VerifyFormating beautiofy/HTML-CSS-JS, 
- jscs (from gulp)
- eslintrc from starter kit? ammend or fix, or use defaults
-Basic script
-Gulpify ?
-Basic test
-Use ES6/7 features
  - Arrow functions
  - Async/Await - with promises
-RxJS

## Global Sublime setup

  - npm install -g eslint eslint-plugin-babel
  - added "eslintrc to "js": { "allowed_file_extensions": ["js", "json", "eslintrc", ....],
  - Also set .eslintrc as JSON Syntax
  - install package SublimeLinter-contrib-eslint
  - disable jshint in package SublimeLinter-User settings
  - install package babel, and babel-snippets for sublime
