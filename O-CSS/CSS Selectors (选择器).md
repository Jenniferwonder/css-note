---
Title: CSS Selectors (选择器)
Type: D
tags:
  - CSS
status: 
DateStarted: 2023-09-19
DateModified: 2023-09-21
mindmap-plugin: basic
DateDone: 2023-09-19T00:00:00.000+08:00
---

# [[O-CSS|CSS]] Selectors (选择器)

## Selector List

### combine these into a selector list, by adding a **comma** between them

### `h1, .special { color: blue;}`

## Universal Selector

### `*`

### reset stylesheets
- to remove the margins on all elements
- strip out all of the browser styling

### make your selectors easier to read, making it more obvious what the selector is doing
- `article *:first-child`{ }

### Global Style (全局样式设置)

## Element Selector (Type/ Tag name selector)

### `p, li, h1 { }`

### `body`

### `html`

## ID Selector

### `#onething`

### can be used only **once per page**, and elements can only have **a single id value** applied to them

### It can select an element that has the id set on it

### To only target the element without applying the block rules, precede the ID with a Type Selector
- `h1#heading {color: purple;}`
    - ‼️ The color will not be set to purple

### an ID has high specificity. It will overrule most other selectors.

### In most cases, it is preferable to add a **class** to an element instead of an ID

## Class Selector

### `.className{ }`

### select a subset of the elements without changing the others

### Targeting classes on particular elements
- `h1.highlight {background-color: pink;}`
- The rule will only apply to that particular element and class combination

### Target an element if it has more than one class applied
- `.notebox.warning {border-color: orange; font-weight: bold;}`

## Attribute Selector

### `a[title] {}`
- select elements based on a certain attribute on an element

### `a[href="https://example.com"] {}`
- make a selection based on the presence of an attribute with a particular value

### `p[class~="special"]`
- Matches elements with an attr attribute whose value is exactly value, or contains value in its (space separated) list of values.

### `div[lang|="zh"]`
- Matches elements with an attr attribute whose value is exactly value or begins with value immediately followed by a hyphen.

### `li[class^="box-"]`
- Matches elements with an attr attribute, whose value begins with value.

### `li[class$="-box"]`
- Matches elements with an attr attribute whose value ends with value.

### `li[class*="box"]`
- Matches elements with an attr attribute whose value contains value anywhere within the string.

### 📌Case-sensitivity
- To match case-insensitive
    - use the value `i `before the closing bracket
    - `li[class^="a" i] { }`

## pseudo-classes (伪类)

### Style **certain states** of an element
- as if you had added a class for that state to the DOM

### User-action Pseudo Class (Anchor element states)
- `<a href="http://example.com">link</a>`
- `:linked, :visited`
    - ! Set basic properties
    - unvisited, visited
- `a:hover {text-decoration: none;}`
    - being hovered over
- `:focus`
    - focused via the keyboard
- `:active`
    - in the process of being clicked (activated)
    - ! When a button is clicked

### Simple Pseudo Class
- `:first-child`
- `:last-child`
- `:only-child`
- `:invalid`

### 📌  It is valid to write pseudo-classes and elements without any element selector preceding them
- the rule would apply to any element that belongs to the class

## pseudo-elements (伪元素)

### Select **a certain part of an element** rather than the element itself
- Act as if you had added a whole new HTML element into the markup, rather than applying a class to existing elements

### **`p::first-line{ }`**
- Selects the first line of text inside an element
- If the number of words increases or decreases it will still only select the first line

### To Generate Content
- `content:""`
    - The property must be used along with
    - Whenever you see these selectors, look at the content property to see what is being added to the HTML element.
- `::before`
- `::after`
    - ! Set other properties to make sure it's identical to the button parent
        - display: in-line block
        - height: 100%
        - width: 100%
        - border-radius: 100px
    - ! Set its position behind the buttons
        - position: absolute
            - ! for child element
    - `:hover::after`
- 📌to insert an icon
    - `.box::after {content: " ➥";}`
        - a visual indicator that we wouldn't want read out by a screen reader
- 📌to insert an empty string
    - set this to `display: block` in order that we can style it with a width and height. We then use CSS to style it just like any element
- 📌Example: [CSS Arrow Box](https://cssarrowplease.com/)

## Combining pseudo-classes and pseudo-elements

### `article p:first-child::first-line { }`

## Combinators

### ⭐Descendant combinator
- `li em {color: rebeccapurple;}`
    - To select only an `<em>` that is nested inside an `<li>` element

### ⭐ Child combinator
- `article > p { }`
    - selects only **the direct children**

### ⭐Adjacent sibling combinator
- `h1 + p {font-size: 200%;}`
    - styling a paragraph when it comes directly after a heading at the same hierarchy level

### ⭐ General sibling combinator
- `p ~ img`
    - select **siblings of an element even if they are not directly adjacen**

### 📌you can combine multiple selectors and combinators together
- `article p span {}`
    - `/* selects any <span> that is inside a <p>, which is inside an <article> */`
- `h1 + ul + p { }`
    - `/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1> */`

### 📌 Nesting to create complex selectors
- ![[Paste image 1695097054773image.png]]

## 📌 Reference

### [Level 3 Selectors specification](https://www.w3.org/TR/selectors-3/)

### [ Level 4 Selectors specification](https://www.w3.org/TR/selectors-4/)