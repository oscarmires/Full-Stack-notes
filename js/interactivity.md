# Interactive websites with JS
## The `<script>` element
Attributes:
- `defer`: execute only after HTML file is completely parsed. (Load but not execute)
- `async`: load and execute code asynchronously with the rest of webpage.
- `src`

## Console commands / keywords
- `document`: returns DOM
- `alert`: show message pop-up
- `.innerHTML`: access content of element. Can also be used to add HTML code to an element.
- `.querySelector()`: access element using CSS selector (first element that matches)
- `.getElementById()`
- `.style.[property]`: access to inline style of HTML tag
- `.createElement(tagName)`: creates, but doesn't append to tree. To append: `.appendChild()`
- `.removeChild()`: receives some element accessed through (ex.) .querySelector()
- `.hidden`: bool
- For traversing: `.parentNode`, `.firstChild`, `.children`


## Elements in th DOM
There are nine different types of node objects in the DOM tree:
- Element
- Text
- ...

## The _Element_ Node
Attributes can be accessed from DOM
- class
- id
- style
- ...

## Event handler functions
- `.addEventListener()`: make _event target_ liste to speceific event and execute handler function
- `.on`_`event`_: ex. .onclick;
- `.removeEventListener()`

## Event object
Properties:
- .target
- .type
- .timeStamp

## Mouse events
- .onwheel
- .onclick
- .onmousedown (mousedown)
- .onmouseup (mouseup)
- .onmouseover (mouseover)
- .onmouseout (mouseout)