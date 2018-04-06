
# webpack-watch-files-plugin

[![Build Status](https://travis-ci.org/Fridus/webpack-watch-files-plugin.svg?branch=master)](https://travis-ci.org/Fridus/webpack-watch-files-plugin)

Webpack watch additional files. This plugin can trigger a build when these files change.
Le livereload sera déclenché si vous l'utilisez mais ne fonctionne pas avec HRM

## Installation

```sh
npm i --save-dev webpack-watch-files-plugin
```

## Options

- `files` - (Default `[]`) Array of patterns
- `verbose` - (Default `false`) List files found

## Usage

```js
import WatchExternalFilesPlugin from 'webpack-watch-files-plugin'

const config = {
  // ... webpack config ...
  plugins: [
    // ....
    new WatchExternalFilesPlugin({
      files: [
        './src/**/*.js',
        '!./src/*.test.js'
      ]
    })
  ]
}
```
