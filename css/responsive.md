# Responsive design

## Relatively sized content
| Unit | Description |
| ---- | ----------- |
| em | From "em" (letter M) - represents the font-size of the current element |
| rem | "Root em" - relative to root's (<html>) font-size, which is usually 16px;

## Media scale design pattern
```css
.container {
  width: 50%;
  height: 200px;
  overflow: hidden;
}
 
.container img {
  max-width: 100%;
  height: auto;
  display: block;
}
```
## Percentages
It's a measure relative to the parents **width**.

## Media Queries
```css
@media only screen and (min-width: 320px) { 
    /* ruleset for >= 320px */
}
 
 
@media only screen and (min-width: 480px) { 
    /* ruleset for >= 480px */
}
```
* `min/max-width`: target screen size
* `min/max-resolution`: target screen resolution

`and` (AND) and `,` (OR) can be used to specify the conditions that must be met.  

Evaluate orientation:
```css
(orientation: vertical)
(orientation: landscape)
```

![Common screen sizes](https://content.codecademy.com/courses/freelance-1/unit-5/screen-sizes.png)

### Breakpoint-oriented design
Instead of thinking in a different media query for every single device possible, think of a media query for the breakpoints — the limits at which content collapses.

## Responsive nav design patterns
Read: https://responsivenavigation.net
