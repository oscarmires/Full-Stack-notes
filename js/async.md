# Asynchronous JavaScript

> JavaScript is traditionally single-threaded. Even with multiple cores, you could only get it to run tasks on a single thread, called the main thread.

**Main thread** handles user input/output and access to DOM.

## Aync callbacks

> Functions that are specified as arguments when calling a function which will start executing code in the background.

Example:  
```js
function loadAsset(url, type, callback) {
  let xhr = new XMLHttpRequest();
  xhr.open('GET', url);
  xhr.responseType = type;

  xhr.onload = function() {
    callback(xhr.response);
  };

  xhr.send();
}

function displayImage(blob) {
  let objectURL = URL.createObjectURL(blob);

  let image = document.createElement('img');
  image.src = objectURL;
  document.body.appendChild(image);
}

loadAsset('coffee.jpg', 'blob', displayImage);
```

## Promises
The new style of async code.
- `.then(onFullfilled(response), onRejected(response))`: will run the callback after previous async operation (promise). It always returns a promise
- `.catch(error)`: handle error. To be used instead of `onRejected()`  

\* _Composition_: the process of chaining promises together.

### Promise objects
Possible states:
- pending
- fulfilled (settled): now has a resolved value
- rejected (settled): operation failed, this is usually an error
- `.then()` and `.catch()` are methods of the Promise object.

### Creating a promise
```js
const executorFunction = (resolve, reject) => { };
const myFirstPromise = new Promise(executorFunction);
```
\* `executorFunction` automatically runs when Promise's constructor is called.

### `resolve(val)`
- changes promise's status to fulfilled
- sets promise's resolve value to the argument passed

### `reject(reason)`
- changes promise's status to rejected
- sets promise's rejected reason to argument passed

Example:
```js
const executorFunction = (resolve, reject) => {
  if (someCondition) {
      resolve('I resolved!');
  } else {
      reject('I rejected!'); 
  }
}
const myFirstPromise = new Promise(executorFunction);
```

### Promise.all()
Run multiple asynchronous events (_concurrency_) no matter the order, but all should resolve before proceeding to `then()`.
```js
let myPromises = Promise.all([returnsPromOne(), returnsPromTwo(), returnsPromThree()]);
 
myPromises
  .then((arrayOfValues) => {
    console.log(arrayOfValues);
  })
  .catch((rejectionReason) => {
    console.log(rejectionReason);
  });
  ```

## Cooperative asynchronous code
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Timeouts_and_intervals
- `let t = setTimeout(func, ms, param1, param2, ...)`: Execute a specified block of code once after a specified time has elapsed.
    - > Guarantees the given delay between the code execution completion
    - `clearTimeout(t)`: cancel timeout
- `let t = setInterval(func, ms, param1, param2, ...)`: Execute a specified block of code repeatedly with a fixed time delay between each call.
    - > The interval _includes_ the time taken to execute the code
    - `clearInterval(t)`: cancel interval
- `requestAnimationFrame()`: specialized enqueueing function created for running **animations** efficiently in the browser
