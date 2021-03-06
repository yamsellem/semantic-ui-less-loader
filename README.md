# Usage

Use semantic-ui-less-loader instead of less-loader.

```js
const path = require('path');

const webpackConfig = {
    context: __dirname,
    entry: './src/semantic.less',
    module: {
        loaders: [
            {
                test: /[.]less$/,
                loader: 'style-loader!css-loader!semantic-ui-less-loader?sourceMap',
            },
         ],
    },
    semanticUILessLoader: {
        siteFolder: path.join(__dirname, 'src/site'),
    },
};

module.exports = webpackConfig;
```

# Options

- defaultFolder (default: /path/to/node_modules/semantic-ui-less)
- siteFolder (default: ${defaultFolder}/_site)
- definitionsFolder (default: ${defaultFolder}/definitions)
- themesFolder (default: ${defaultFolder}/themes)
- themeConfigPath (default: ${defaultFolder}/theme.config.example)
- themePath (default: ${defaultFolder}/theme.less)
