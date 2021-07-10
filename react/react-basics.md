# React basics

https://vimeo.com/542610281

## Imports
```js
import React from 'react';
import ReactDOM from 'react-dom';
```

## JSX
>syntax extension

JSX code is interpreted by a JSX compiler, which translates it into JavaScript.

## VirtualDOM
Abstraction of the "real DOM" that optimizes changes in the HTML page
```js
ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
``` 
## Keys

Not all lists need to have keys. A list needs keys if either of the following are true:

1. The list-items have memory from one render to the next. For instance, when a to-do list renders, each item must “remember” whether it was checked off. The items shouldn’t get amnesia when they render.
2. A list’s order might be shuffled. For instance, a list of search results might be shuffled from one render to the next.

