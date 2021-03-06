lang-detector  [![Build Status](https://travis-ci.org/hosein2398/lang-detector.svg?branch=master)](https://travis-ci.org/hosein2398/lang-detector) [![npm downloads](https://img.shields.io/npm/v/lang-detector.svg)](https://www.npmjs.com/package/lang-detector) [![Software License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
=====

![lang-detector](https://raw.githubusercontent.com/hosein2398/File-Container/master/Lang-detector/Lang-detector.png)

A fast and small library for detecting the programming language of a code snippet. 
Can be used for strings of code spanning multiple thousand lines.

This library should only be used if you don't have anything else to go by to determine the language of the code, like a file extension.
## Demo 
[Here](https://hosein2398.github.io/lang-detect/) you can see demo of this project.

## Detectable languages
* JavaScript
* C
* C++
* Python
* Java
* HTML
* CSS
* Ruby
* Go
* PHP

## Install
```Shell
npm install lang-detector --save
```

## Usage
```JavaScript
/**
 * function detectLang(snippet, options) { ... }
 *
 * @snippet {String} The code snippet.
 * @options {Object} (Optional) {
 *   heuristic: {Boolean} Enable heuristic optimisation for better performance. `true` by default.
 *   statistics: {Boolean} Return statistics. `false` by default.
 * }
 * @return {String} (Name of the detected language) or {Object} (Statistics).
 */
var detectLang = require('lang-detector');

detectLang('List<String> things = new ArrayList<>();')
    // =>    'Java'
detectLang('console.log("Hello world");')
    // =>    'JavaScript'
detectLang('Hello world.', { statistics: true })
    /* =>   {
                "detected": "Unknown",
                "statistics": {
                    "JavaScript": 0,
                    "C": 0,
                    "C++": 0,
                    "Python": 0,
                     ...
                    "Unknown": 1
                }
            } 
     */
```

## Unit tests
Run `npm test` in the root of the directory to run the tests.

## License
<a href="https://tldrlegal.com/license/mit-license" target="_blank">MIT</a> © <a href="https://github.com/ts95/" target="_blank">Toni Sučić</a>