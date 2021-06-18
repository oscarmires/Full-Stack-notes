# Modules
"Reusable pieces of code that can be exported/imported"

## Node.js 
### `module.exports`
make module available to another file
1. Create an object to represent module
2. Add properties/methods
3. Export module with module.exports  

### `require(path)`
Import module from different file
1. import module with `require()` and assign to variable
2. use module

## ES6
Used for front-end development
### default exports
Use `export default [object]`, works similar to module.exports
### named imports
Use `import [moduleVar] from [path]`, works similar to require
### named exports
To export data through the use of variables.  
Use `export {var1, var2, ...}` or by using _export_ keyword in front of variable declaration
## named imports
To import named exports from other file
Use `import {var1, var2, ...}`
