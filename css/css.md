# CSS: Cascading Style Seets

## Adding the CSS dimension

### Inline styles
```html
<p style="color: red; font-size: 20px;">I'm learning to code!</p>
```  
### `<style>` head section
```html
<style>
p {
    font-family: Arial;
}
</style>
```
### .css files
```html
<link href="syles.css" type="text/css" rel="stylesheet">
```

## Definitions
- selector: element outer structure in css that represents tags in html, e.g. `p { ... }` for `<p>`
    - select by class: `.class { }`
    - select by ID: `#id-name { }`
- declaration: statement within selector that consists if _property_ and _value_
- rule: a selector and its declarations


## Text
### Font properties
- font-family
- font-size
- font-weight: light/medium/bold/100-900
- font-style: italic/normal

### Text and parragraph properties
- text-transform: capitalize, uppercase, lowercase, etc.
- word-spacing
- line-height: accepts unitless value - line-height-font-size ratio

### Fallback fonts
`font-family: "Option 1", "Option 2", serif/sans-serif;`

### @font-face {}
An alternative to linking fonts to use them.
To get the @font-face, copy the /* latin */ labelled section of code that appears when browsing the _google fonts_ link
@font-face is also useful for using local fonts. A relative path to the font file (ex. .woff2 or .ttf) is required

## Other popular properties
- color (foreground)
- background-color
- opacity
- background-image (specify path with _url()_)

## Units
*Note that many properties that manage numeric values usually add the provided value to the default (not set it equal)
- px
- em: relative to font size
- rem: relative to the font size of the root elemnt


## Selector specificity
### Hierarchy
1. more important: ID selectors
2. class selectors
3. less important: tag selectors

### Chaining selectors
Combine multiple selectors
```CSS
h1.special {
 
}
```
the selector refers to an element between h1 tags and which class is "special"
### Nested element selectors
Select nested elements
```CSS
.main-list li {
 
}
```
### Multiple selectors
Separate multiple selectors by comma to apply same style to all
```CSS
h1, 
.menu {
  font-family: Georgia;
}
```

## Special elements
- _url()_ - specify path as value in some property
- !important - apply this rule no matter the specificity of other elements 

## Initial reset
To reset initial _user agent stylesheets_:
```CSS
* {
  margin: 0;
  padding: 0;
}
```

## Box model
Use std box model: `box-sizing: content-box;`  
Use alt box model: `box-sizing: border-box;`  

## Visibility
Hide element (still displays space): `visibility: hidden;`  
Remove element completely: `display: none;`  

## Center elements
To ceneter an element within its container: `margin: 0 auto;`  

## Clearfix hack
Make a container use floating child elements' dimensions.
https://www.youtube.com/watch?v=8G0cZNJEy6E
```css
.group:after {
  content: "";
  display: block;
  clear: both;
}

/* or */

.group:after {
  content: "";
  display: table;
  clear: both;
}
```

