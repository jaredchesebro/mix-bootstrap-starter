# mix-bootstrap-starter
Starter project for Bootstrap Framework via Laravel Mix

## CLI Commands
- `npm run dev` == `npx mix`
- `npm run watch` == `npx mix watch`
- `npm run production` == `npx mix --production`

## Errors
Add the following to your webpack.mix.js for verbose error reporting:
```
// webpack.mix.js
mix.webpackConfig({
    plugins: [],
    resolve: {},
    // Display compilation errors
    stats: {children: true}
});
```
## Versioning
In order to append the version string to your main.css and main.js you'll need to install/write a plugin that will do it at runtime. Here's a couple examples:
- ExpressionEngine: [mixeer](https://github.com/benjivm/mixeer)
- Craft CMS: [Mix](https://plugins.craftcms.com/mix?craft4)

## JQuery
If you need jquery install it via npm and add the following code to `main.js` and `webpack.mix.js` respectively:
``` 
// main.js
global.$ = global.jQuery = require('jquery');
```

```
// webpack.mix.js
mix.autoload({
    // Autoload JQuery
    jquery: ['$', 'jQuery', 'window.jQuery'],
});
```
