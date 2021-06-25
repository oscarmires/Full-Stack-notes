# Mocha
Test framework for js  
https://mochajs.org

## Setup
```
$ npm init
$ npm install mocha -D
```
\* `-D` notes that this package is a dependency for your project, which makes it easier for other developers to use

## Call 
To run the tests.. 

Option 1:
```
$ ./node_modules/mocha/bin/mocha
```
Option 2 (recommended):
In `package.json`...
```
"scripts": {
  "test": "mocha"
}
```
\* Option 2 allows to call using command `npm test`

## Creating tests
- import: `const assert = require('assert');`
- `describe(string, func)`: organize tests into nested groups
- `it(string, func)`: unit test - human-readable string

## Setup, exercise, verify
Example:
```js
// 3 phase approach
describe('.pop', () => {
  it('returns the last element in the array [3phase]', () => {
    // Setup
    const knightString = 'knight';
    const jediPath = ['padawan', knightString];

    // Exercise
    const popped = pop(jediPath);

    // Verify
    assert.ok(popped === knightString);
  });
});
```

## Teardown and hooks
>Teardown: reset any conditions that were changed during the test

>Hook: a piece of code that is executed when a certain event happens.

Example (no hooks):
```js
const assert = require('assert');
const fs = require('fs');

describe('appendFileSync', () => {
  it('writes a string to text file at given path name', () => {

    // Setup
    const path = './message.txt';
    const str = 'Hello Node.js';
    
    // Exercise: write to file
    fs.appendFileSync(path, str);

    // Verify: compare file contents to string
    const contents = fs.readFileSync(path);

    assert.ok(contents.toString() === str);

    // Teardown: delete path
    fs.unlinkSync(path);
  });
});

```

Example (hooks enhancement):
```js
describe('example', () => {
 
  afterEach(() => {
    // teardown goes here
  });
 
  it('.sample', () => {
    // test goes here
  });
});
```

## Assert
Documentation: https://nodejs.org/api/assert.html
- `.ok(bool)`
- `.equal(result, expected)` - loose equality
- `.strictEqual(result, expected)` - strict equality
- `.deepEqual(obj1, obj2)` - loose equality
