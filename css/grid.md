# CSS Grid

## Three mayor components
- Columns: vertical sections
- Gutter: negative space between each column
- Margin: margin

## Whitespace
- Passive / micro whitespace: improve aesthetics
- Active / macro whitespace: enhance overall structure and guide users

## CSS grid properties

Display
```css
display: grid /* For block-level */
display: inline-grid /* For inline-level */
```

By default, grids contain **one column**. This property is used to define number of columns:
```css
grid-template-columns: [first column width] [second column width] [...]
```

To specify the number and size of rows:
```css
grid-template-rows: [first row height] [second row height] [...]
```

Shorthand to rows and columns:
```css
grid-template: [first row height] [second row height] [...] / [first column width] [second column width] [...]
```

The **fr (fraction) unit**
- Adds all fr's
- Devides containers width or height by the previous sum
- Assigns each column or row its corresponding part
```css
grid-template: 2fr 1fr 1fr / 1fr 3fr 1fr;
```
In the example, first row occupies 2 parts, second row occupies 1 part, etc.

The **repeat()** function
```css
grid-template-columns: repeat(3, 1fr);
```
Ex. creates three columns.

The **minmax()** function
```css
grid-template-columns: minmax(100px, 200px);
```
Ex. creates one column min-width: 100px and max-width: 200px.

Space between gaps:
```css
/* row */
grid-row-gap: [gap];
/* column */
grid-column-gap: [gap];
/* shorthand */
grid-gap: [row gap] [column gap];
```

Span single grid elements into multiple columns or rows:
```css
.item {
  grid-row-start: 1;
  grid-row-end: 3;
  grid-column-start: 4;
  grid-column-end: span 2;
  /* shorthand */
  grid-row: 1 / 3;
  grid-column: 4 / span 2;
  grid-area: 1 / 4 / 3 / span 2;
}
```
