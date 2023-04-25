# webpack-demo

an exercise to learn _webpack_ (a *static module bundler* for modern JavaScript applications).

[Getting Started](https://webpack.js.org/guides/getting-started/)

## 1. Basic Setup

```sh
$ mkdir webpack-demo
$ cd webpack-demo

$ node -v
v14.15.3

$ npm init -y
$ npm install webpack webpack-cli --save-dev
```

## 2. Project
```sh
# Structure
 webpack-demo
  |- package.json
  |- package-lock.json
 |- index.html
 |- /src
   |- index.js

# Change
 webpack-demo
  |- package.json
  |- package-lock.json
 |- /dist
   |- index.html
  |- /src
    |- index.js

```

## Dependencies

```sh
$ npm install --save lodash

$ npx webpack
asset main.js 69.5 KiB [emitted] [minimized] (name: main) 1 related asset
runtime modules 1010 bytes 5 modules
cacheable modules 532 KiB
  ./src/index.js 270 bytes [built] [code generated]
  ./node_modules/lodash/lodash.js 531 KiB [built] [code generated]

WARNING in configuration
The 'mode' option has not been set, webpack will fallback to 'production' for this value.
Set 'mode' option to 'development' or 'production' to enable defaults for each environment.
You can also set it to 'none' to disable any default behavior. Learn more: https://webpack.js.org/configuration/mode/ 

webpack 5.80.0 compiled with 1 warning in 1649 ms
```

## 3. Webpack configuration

```sh
webpack-demo
  |- package.json
  |- package-lock.json
 |- webpack.config.js
  |- /dist
    |- index.html
  |- /src
    |- index.js

$ npx webpack --config webpack.config.js
asset main.js 69.5 KiB [compared for emit] [minimized] (name: main) 1 related asset
runtime modules 1010 bytes 5 modules
cacheable modules 532 KiB
  ./src/index.js 268 bytes [built] [code generated]
  ./node_modules/lodash/lodash.js 531 KiB [built] [code generated]

WARNING in configuration
The 'mode' option has not been set, webpack will fallback to 'production' for this value.
Set 'mode' option to 'development' or 'production' to enable defaults for each environment.
You can also set it to 'none' to disable any default behavior. Learn more: https://webpack.js.org/configuration/mode/ 

webpack 5.80.0 compiled with 1 warning in 1889 ms
```