<h3 align='center'>webpack中压缩资源的插件</h3>

* HTML
  - [HtmlWebpackPlugin](https://www.npmjs.com/package/html-webpack-plugin)

  ```js
  const HtmlWebpackPlugin = require('html-webpack-plugin')

  module.exports = {
    entry: 'index.js',
    output: {
      path: __dirname + '/dist',
      filename: 'index_bundle.js'
    },
    plugins: [
      new HtmlWebpackPlugin()
    ]
  }
  ```
  
* CSS
  - [MiniCssExtractPlugin](https://www.npmjs.com/package/mini-css-extract-plugin)

  ```js
  const MiniCssExtractPlugin = require('mini-css-extract-plugin');

  module.exports = {
    plugins: [new MiniCssExtractPlugin()],
    module: {
      rules: [
        {
          test: /\.css$/i,
          use: [MiniCssExtractPlugin.loader, 'css-loader'],
        },
      ],
    },
  };
  ```

* JavaScript
  - [UglifyPlugin](https://www.npmjs.com/package/uglify-js-plugin)

  ```js
  var UglifyJsPlugin = require('uglify-js-plugin');
 
  module.exports = {
      entry: {
          hello: './src/hello.js'
      },
      output: {
          path: './build',
          filename: '[name].js'
      },
      plugins: [
          new UglifyJsPlugin({
              compress: true, //default 'true', you can pass 'false' to disable this plugin
              debug: true //default 'false', it will display some information in console
          })
      ]
  };
  ```