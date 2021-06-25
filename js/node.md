# Node
The **Node** runtime environment was created for the purpose of executing JavaScript code without a browser

## Runtime environments
> A runtime environment is an instance of the execution model. They acta as a small operating system.

Javascript runs in RE's such as:
- Web browsers
- Node


## Features 

- Access to the server's file system
- "" Database
- "" Network

Other features are not available, such as the _window_ object.

## Modules
Some implementations are:
- For Node, use `modules.exports` along with `require()` syntax.
- For browser's runtime env. use `import`/`export`. More on how to use this syntax [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules).

**In Node:**
1. Create module by creating js file
2. Add functions as properties of the `module.exports` object:
```js
/* converters.js */
function celsiusToFahrenheit(celsius) {
  return celsius * (9/5) + 32;
}
 
module.exports.celsiusToFahrenheit = celsiusToFahrenheit;
```
3. In another file, assign to a variable a module provided by `require(file_path)` function.
4. (Optional) Use **object destructuring** to import specific function:
```js
/* celsius-to-fahrenheit.js */
const { celsiusToFahrenheit } = require('./converters.js');
 
const celsiusInput = process.argv[2]; 
const fahrenheitValue = celsiusToFahrenheit(input);
```

**In ES6 (Web browsers):**
1. Create module by creating js file
2. Use _named exports_ syntax to export functions:
```js
export { resourceToExportA, resourceToExportB, ...};
```
3. (Optional) Individual values may be exported as named exports by simply placing the `export` keyword in front of the variable’s declaration.
```js
/* dom-functions.js */
export const toggleHiddenElement = (domElement) => {
  // logic omitted...
}
 
export const changeToFunkyColor = (domElement) => {
  // logic omitted...
}
```
4. Import module:
```js
import { exportedResourceA, exportedResourceB } from '/path/to/module.js';
// or...
import { exportedResource as newlyNamedResource } from '/path/to/module'
```
5. Add attribute `type="module"` to script in HTML:
```
<script type="module" src="./path/to/module.js"> </script>
```

### `import`/`export` objects (default)
```js
// in 'module.js'...
const resources = {
  valueA,
  valueB
}
export default resources;
// or
export { resources as default };

// in other javascript file...
// This will work...
import resources from 'module.js'
const { valueA, valueB } = resources;
 
// This will not work...
import { valueA, valueB } from 'module.js'
```
