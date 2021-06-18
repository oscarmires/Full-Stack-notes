# Flexbox

There are two important components to a flexbox layout: flex containers and flex items.

"A flex container’s children are flex items!"

```css
div.container {
  display: flex;
}
```
- `display: flex;` makes container a flex container.
    - It's children will appear "inline"
    - The container will remain __block level__
- `display: inline-flex;` makes a container a flex container.
    - It's children will appear "inline"
    - The container will behave as __inline__ element


## Handling size

"The size of the parent container will override the size of its child elements."
- Flex children elements shrink in order to fit parent's width

## `justify-content`
Position items horizontaly.
### Values
- `flex-start`: [default] in order from left to right, no space before/between
- `flex-end`: last item right to left, no space before/between
- `center`: centered, no space before/between
- `space-around`: equal space before/after items
- `space-between`: equal space between, not before/after

## `align-items`
Position items vertically.
### Values
- `flex-start`: in order from top
- `flex-end`: from bottom
- `center`: centered
- `baseline`: "the bottom of the content of all items will be aligned with each other."
- `stretch`: [default] stretch to fill
    - respects `max-height`, `height`

## `flex-wrap`
Move to next line instead of shrinking elements
### Values
- `wrap`: items go to new line below.
- `wrap-reverse`: items go to new line above.
- `nowrap`: [default] don't go to new line.

## `align-content`
Space rows along the cross axis. It can take same 6 values of `align-items`.

## Flex-flow shorthand for containers
`flex-flow: [flex-direction] [flex-wrap]`

## Flex items' properties
Properties that are declared in flex items, not containers.
- `flex-grow: #;` where # is an integer, specifies which items should grow more or less (proportionally) than others.
    - respects `max-width`
    - 0 means don't grow
- `flex-shrink: #;` where # is an integer, specifies which items should shrink more or less (proportionally) than others.
    - respects `max-width`
    - 0 means don't shrink
- `flex-basis`: to be used instead of width. Specifies width before growing/shrinking

## Flex shorthand for items properties
`flex: [grow] [shirnk] [basis]`

## Axes

|  | Main | Cross |
| ---- | ---- | ----- |
Applicable properties | justify-content, flex-wrap, flex-grow, flex-shrink | align-items, align-content |

### `flex-direction`
Interchange main and cross axes.  
Values:
- `row`: [default] from left to right starting from top left corner
- `row-reverse`: from right to left starting from top right corner
- `column`: from top to bottom starting from top left corner (main axis is vertical)
- `column-reverse`: from bottom to top starting from bottom left corner
