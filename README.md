#### Loader for creating a banner and footer similar to [grunt-contrib-concat](https://github.com/gruntjs/grunt-contrib-concat)

#### Example Usage
```js
var injectParams ='inject=' + encodeURIComponent('var targetName = __filename.replace("website-guts/assets/js/", "");\n\n') +
    '&banner=' + encodeURIComponent(banner) +
    '&footer=' + encodeURIComponent(footer);
```

In `webpack.config.js`
```js
  module: {
    loaders: {
      test: /\.js$/,
      exclude: [
        /node_modules/,
        /bower_components/,
      ],
      loader: 'inject-filename-loader?' + injectParams
    }
  }
```


