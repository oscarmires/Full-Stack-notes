# React basics

React is a JavaScript front-end library. Authored by Jordan Walke.  
Cheatsheet: https://devhints.io/react

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

## Conditionals
(not React-specific)
```js
// OR - yields first truthy value in list
{<h1>{title || 'Click an animal for a fun fact'}</h1>}
// AND - yields second value if expr is true
{expr && 'hi'}
```

## `props` ("properties")
If you want to pass information that isn’t a string, then wrap that information in curly braces. Ex:
```js
<Greeting myInfo={["top", "secret", "lol"]} />
```

\* Handler / events naming convention:
- use _on-_[eventName] to name prop
- use _handle_-[eventName] to name handler function


## `this.props.children`
>will return everything in between a component’s opening and closing JSX tags.
- no children: returns `undefined`
- one child: returns child
- \>1 child: returns **array** of children


## Default props
Give default value to props (in case they aren't passed)
```js
Example.defaultProps = { text: 'yo' }; 
```

## State
Change state with:
```js
// always automatically calls render()
this.setState(obj);
```
Bind event handlers that use this:
```js
// in constructor:
this.eventHandler = this.eventHandler.bind(this);
```
>with **bind** any further arguments [like _e_] are automatically forwarded. (Arrow functions need to pass _e_)
