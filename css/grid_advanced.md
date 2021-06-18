# CSS Grid (advanced)

## `grid-template-areas`
Declare rows and columns using names.
```css
grid-template-areas:    "head head"
                        "nav nav" 
                        "info services"
                        "footer footer";
```

##  `grid-template-rows` / `-columns`
Declare grid tamplate's rows and columns' sizes
```css
grid-template-rows: 300px 120px 800px 120px;
grid-template-columns: 1fr 3fr; 
```

## `grid-area`
Define the grid area that an element will span.
```css
gird-area: head;
```

## Overlap
Use `z-index` to overlap.

## Justify
- `justify-contents`: position elements in row axis within columns.
- `justify-items`: position entire grid within its container
- `justify-self`: individual grid element level justify

## Align
- `align-contents`: position elements in column axis within columns.
- `align-items`: position entire grid within its container (vertically)
- `align-self`: individual grid element level alignment

## Implicit and explicit grids
The implicit grid is an algorithm built into the specification for CSS Grid that determines default behavior for the placement of elements when there are more than fit into the grid specified by the CSS.

The default behavior of the implicit grid is as follows: items fill up rows first, adding new rows as necessary.

| auto element property description | specification |
| --------------------- | ------------- |
| height | `grid-auto-rows`, `grid-auto-columns` |
| rendering order | `grid-auto-flow` |

## Extra resources
https://css-tricks.com/snippets/css/complete-guide-grid/#top-of-site

