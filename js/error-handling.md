# Error handling

## Errors
JavaScript errors are objects that have a name and message property.  
Types of errors: SyntaxError, TypeError, ReferenceError.

* To create an error, use `Error('message')` constructor
* Use `throw` keyword to throw the error:
```js
throw Error('Something wrong happened');
```
## `try...catch...finally`
- A variable that represents an error is passed to the `catch`
- `finally` executes always regardless of the error thrown or catched. This statement is **optional**.
```js
try {
  throw Error('This error will get caught');
} catch (e) {
  console.log(e);
}
```
