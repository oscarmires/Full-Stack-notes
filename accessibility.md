# Accessibility

https://www.boia.org/blog/what-is-a11y

>Accessibility refers to designing devices, products, and environments such that individuals with disabilities or sensory impairments can successfully use the device or product.

- [Accessibility guidelines](https://www.w3.org/TR/WCAG21/)
- [Color contrast checker](https://webaim.org/resources/contrastchecker/)
- [A11y checklist](https://www.a11yproject.com/checklist/#header)

## ARIA (Accessibile Rich Internet Applications)
Guidelines for making information on the internet accessible to all.
### 1. Semanitc HTML elements
Example:
> The **header** tag is intended to contain introductory and navigational elements such as a logo, links, or a search bar.

[HTML element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

### 2. ARIA Roles
>To help add context to web page information, ARIA provides an HTML attribute called **role**. The value of an element’s role changes how a screen reader communicates the element.

[ARIA roles reference](https://www.w3.org/TR/html-aria/#allowed-aria-roles-states-and-properties)

**The _presentation_ role**  
The element is just reported in the accessibility tree as a text string with no semantic meaning.

### 3. ARIA Properties
> provide additional information about elements that might not be obvious to users of screen readers.

Example: `aria-label` - gives the screen reader additional information to read out loud to the user.  
Example: `aria-labelledby` - establishes relationships between objects and their label(s), and its value should be one or more element IDs  
...


[Properties reference](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#states_and_properties)


### 4. `alt` ARIA Attribute
- describe images
- describe sources targeted by anchor elements' links
- no more than 150 chars


