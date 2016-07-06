# Node - Babel - ESNext 
Deomnstrate the usage patterns of transpiler (Babel) for a node project.

*This setup is being done as of 2016, with node 6.2.2 and VSCode insiders (tabs finally)*  
*This setup is being done as of 2015-11-06, with node 4.2.1. Babel 6 has just come out.*

Objective/TODO:

+ Minimal setup!
+ VSCode setup
- babel for async/await on node 6
- es2015 for import
- example of linting problems
- example for fixAllErrors (VSCode eslint new feature)
- example of inline hinting/disable/override rule
- npm script targets (lint,watch) exclude gulp.
- npm script targets (start,build,etc... think of docker and dev)
- Is `.editorconfig` still needed?
- Remove references to Sublime in this text.

## Setup:
ESlint/Babel/Formatting

Setup for development cycle of a node module, including setup for transpilation of ES2015 features, and perhaps some experimental feature of ES7, including module loading, testing and editor setup (Sublime).

### VSCode
...  Also check for VSCode formatting compatibility with eslint code style checking
- [Install ESlint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

### VSCode Project

VSCode suggested and made a default `jsconfig.json` file.

`compilerOptions.module: commonjs` shoud be revisited (`es6 | es2015`)

### ESlint

### Babel (with subdir)


## Usage

  gulp test
  gulp watch
  # or
  npm test
  npm run watch

## Setup

- Start using `redux-voting-server` example
- Also look at: https://github.com/elierotenberg/es6-starterkit
- [Lint like it's 2015](https://medium.com/@dan_abramov/lint-like-it-s-2015-6987d44c5b48)

### Babel and node 4.x

I think I have to use [this preset for node4 to get all of es2015](https://github.com/jbach/babel-preset-es2015-node4).

I added these `.babelrc` settings: (stage-3 is to get async working)

    {
      
      "presets": ["es2015-node4","stage-3"]
    }

Use `babel-doctor` to get hints.

### Sublime

- See this [article](https://medium.com/@dan_abramov/lint-like-it-s-2015-6987d44c5b48)
- [Babel-jscs?](https://github.com/jscs-dev/babel-jscs)
- Formatter: not sure yet: 
  - [Sublime JSCS Formatter](https://github.com/TheSavior/SublimeJSCSFormatter) 
  - [esformatter](https://github.com/millermedeiros/esformatter)
  - [esformatter-jsx](https://github.com/royriojas/esformatter-jsx)
  - [sublime-jsfmt](https://github.com/ionutvmi/sublime-jsfmt)

Trying [Sublime JSCS Formatter](https://github.com/TheSavior/SublimeJSCSFormatter), had to edit `/Users/daniel/Library/Application Support/Sublime Text 3/Packages/User/JSCS-Formatter.sublime-settings`

    {
      // Overriden for nvm
      "node_path": {
        "osx": "/Users/daniel/.nvm/current/bin/node"
      },

      "jscs_path": {
        "osx": "/Users/daniel/.nvm/current/bin/jscs"
      }
    }

And I rebound it to `Cmd-shift-[` in `/Users/daniel/Library/Application Support/Sublime Text 3/Packages/User/Default (OSX).sublime-keymap`

    { "keys": ["super+shift+["],  "command": "format_javascript"}

These are the packages which I installed globally to get this working

    npm ls -g --depth=0
      babel-eslint@4.1.4
      eslint@1.9.0
      eslint-plugin-babel@2.1.1
      eslint-plugin-react@3.7.1
      jscs@2.5.1
      jshint@2.8.0

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
