Webpack is a popular module bundler used in many modern web development projects. Setting up a Webpack boilerplate can save time and effort in configuring Webpack for each new project. Here are the steps to set up a basic Webpack boilerplate:

---

1. **Initialize project**: First, initialize a new Node.js project with `npm init`. This will create a `package.json` file which will be used to track project dependencies.
2. **Install Webpack**: Install Webpack as a development dependency using `npm install webpack webpack-cli --save-dev`. This will add Webpack to the project's `package.json` file.
3. **Create configuration files**: Create a `webpack.config.js` file in the root directory of the project. This file will be used to configure Webpack. Here's the configuration you need paste:
```JavaScript
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```
This configuration sets the entry point for the application to `./src/index.js`, and outputs the bundled code to `./dist/bundle.js`.

4. **Create source and distribution directories**: Create a `src` directory to hold the application's source code, and a `dist` directory to hold the distribution code.
5. **Create a script**: Inside the `package.json` file, inside the "scripts" configuration, add the following script to run Webpack:
```
"scripts": {
  "build": "webpack --mode production"
}
```
This script runs Webpack in production mode, which optimizes the output for production.

6. **Test**: Test the Webpack configuration by running `npm run build`. This should generate a bundle.js file in the dist directory. If you see the dist folder then you have successfully installed webpack
