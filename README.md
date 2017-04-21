# npmdoc-universal-webpack

#### api documentation for  [universal-webpack (v0.3.9)](https://github.com/halt-hammerzeit/universal-webpack#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-universal-webpack.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-universal-webpack) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-universal-webpack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-universal-webpack)

#### Isomorphic Webpack

[![NPM](https://nodei.co/npm/universal-webpack.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/universal-webpack)

- [https://npmdoc.github.io/node-npmdoc-universal-webpack/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-universal-webpack/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-universal-webpack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-universal-webpack/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-universal-webpack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-universal-webpack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "universal-webpack",
    "version": "0.3.9",
    "description": "Isomorphic Webpack",
    "main": "index.common.js",
    "module": "index.es6.js",
    "peerDependencies": {
        "webpack": "*",
        "extract-text-webpack-plugin": "^2.0.0-rc.3"
    },
    "dependencies": {
        "colors": "^1.1.2",
        "fs-extra": "^0.30.0",
        "minimist": "^1.2.0",
        "validate-npm-package-name": "^2.2.2"
    },
    "devDependencies": {
        "babel-cli": "^6.6.5",
        "babel-core": "^6.7.2",
        "babel-plugin-transform-react-display-name": "^6.5.0",
        "babel-plugin-transform-runtime": "^6.6.0",
        "babel-preset-es2015": "^6.6.0",
        "babel-preset-react": "^6.5.0",
        "babel-preset-stage-0": "^6.5.0",
        "better-npm-run": "0.0.14",
        "chai": "^3.5.0",
        "extract-text-webpack-plugin": "^1.0.1",
        "istanbul": "^1.1.0-alpha.1",
        "mocha": "^2.5.3",
        "npm-run-all": "^1.4.0",
        "rimraf": "^2.5.0",
        "webpack": "^1.13.1"
    },
    "scripts": {
        "test": "mocha --compilers js:babel-core/register --colors --bail --reporter spec test/ --recursive",
        "test-coverage": "istanbul cover node_modules/mocha/bin/_mocha -- --compilers js:babel-core/register --colors --reporter dot test/ --recursive",
        "test-travis": "istanbul cover node_modules/mocha/bin/_mocha --report lcovonly -- --compilers js:babel-core/register --colors --reporter spec test/ --recursive",
        "clean-for-build": "rimraf ./build/**/*",
        "build-commonjs-modules": "better-npm-run build-commonjs-modules",
        "build-es6-modules": "better-npm-run build-es6-modules",
        "build": "npm-run-all clean-for-build build-commonjs-modules build-es6-modules",
        "prepublish": "npm-run-all build test"
    },
    "betterScripts": {
        "build-commonjs-modules": {
            "command": "babel ./source --out-dir ./build --source-maps",
            "env": {
                "BABEL_ENV": "commonjs"
            }
        },
        "build-es6-modules": {
            "command": "babel ./source --out-dir ./es6 --source-maps",
            "env": {
                "BABEL_ENV": "es6"
            }
        }
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/halt-hammerzeit/universal-webpack.git"
    },
    "keywords": [
        "webpack",
        "isomorphic",
        "universal",
        "render",
        "server",
        "react"
    ],
    "author": "Halt Hammerzeit <halt.hammerzeit.at@gmail.com>",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/halt-hammerzeit/universal-webpack/issues"
    },
    "homepage": "https://github.com/halt-hammerzeit/universal-webpack#readme",
    "bin": {
        "universal-webpack": "./bin/universal-webpack.js"
    },
    "typings": "index.d.ts"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
