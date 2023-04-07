## Install Jest, Babel and JSDOM, and configure them to run tests for your functions

1. **Initialize the project**: You can skip this if you already have a package.json file, else, you need a new npm project by running
```
npm init
```

2. **Start installation**: Install Jest and Babel dependencies by running:
```
npm install --save-dev jest @babel/core @babel/preset-env babel-jest
```

3. **Add Babel Configuration**: Create a new file named '.babelrc' in the root directory of your project and add the following configuration to it
```JSON
{
  "presets": [
    ["@babel/preset-env", {
      "targets": {
        "node": "current"
      }
    }]
  ]
}
```

4. **Update the scripts on your JSON**: Add the following scripts to your package.json file:
```JSON
"scripts": {
  "test": "jest"
}
```

5. **Install JSDOM**: Install the jsdom package as a dev dependency with the following command:
```
npm install --save-dev jsdom
```


🎉 That's it! You should now have Jest and Babel properly installed and configured to run tests for your functions.

Note: Remember in your test file, import the jsdom package, create a new JSDOM instance and assign the window and document objects from the JSDOM instance to the global scope:

```JavaScript
// Your test file

const { JSDOM } = require('jsdom');
const dom = new JSDOM('<!DOCTYPE html><html><body></body></html>');
global.window = dom.window;
global.document = dom.window.document;
```
