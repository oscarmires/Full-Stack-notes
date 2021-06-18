# HTML: HyperText Markup Language
Learn more: https://www.internetingishard.com  
Accesibility: https://medium.com/alistapart/writing-html-with-accessibility-in-mind-a62026493412

## Definitions
HyperText: text that links to other text  
Markup Language: way of anotating text that is distinguishable from the text itself  

## Elements

This is an element:
```html
<p>Hello world!</p>
```
where 
- `<p>` and `</p>` are opening and closing tags, respectively, and
- _Hello World!_ is the content of the element.

## Basic components of HTML document
- `<!DOCTYPE html>` declaration: tells the browser what kind of document to expect (in this case, latest version HTML).
- `<html> ... </html>` tags: optional, but helpful for better interpretation by browser.
- `<head> ... </head>`: contains metadata, which isn't displayed in webpage.
- `<body> ... </body>`: contains everything that is displayed in webpage.

## Components in `<head>` (metadata)
- `<title>`: page title (displayed in tab)
- `<link>`

## Components in `<body>` (semantic)
- `<header>`: usually for either navigational links or introductory content. Can also be in articles or sections.
- `<nav>`: for index
- `<main>`: encapsulates dominant content
- `<footer>`: contact, copyright, terms of use, site map, references, etc.
- `<section>`: define elements such as chapters, headings, etc.
- `<article>`: It holds content that _makes sense on its own_. **Note: can be encapsulated by section**
- `<aside>`: mark additional information that can be used alongside another element.
- `<figure>`: encapsulate media
- `<figcaption>`: describe media (used inside figure)
- `<a>`: anchor - gives the content a hyperlink
- `<audio>`: audio
- `<source>`: specify source, for example, in `<audio>`.
- `<video>`: video

## References to other files
- relative: `"./example.html"` (the period indicates to look for file in current directory).
- absolute: `"https://www.google.com/"`
- within page: `"#section_id"`(# sing indicates link to element with following id)

## Lists
- definition list: `<dl> ... </dl>`, components:
    - `<dl>`: list element title
    - `<dd>`: list element paragraph
- ordered list: `<ol>`, components:
    - `<li>`
- unordered list: `<ul>`, components:
    - `<li>`

## Entities
Display special characters. Example:
- `&lang;` (left angle bracket) displays "<"
- `&amp;` (ampersand) disiplays "&"

## Other components
- `<time>`: specify time through _datetime_ attribute
- `<address>`: specify come contact information like email address

## Comments
```htmal
<!-- This is a comment. -->
```
