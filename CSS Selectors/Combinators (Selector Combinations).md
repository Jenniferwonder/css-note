---
Title: Combinators (Selector Combinations)
Type: D
tags:
  - CSS
DateStarted: 2024-01-09
DateModified: 2024-01-09
DateDo:
DateDone: 2024-01-09T00:00:00.000+08:00
DateDue:
status:
Reviewed: 1
DateReviewed: 2024-01-09T00:00:00.000+08:00
Topic: Selectors
Difficulty: Hard
---

## Combinators (Selector Combinations)

### Combining pseudo-classes and pseudo-elements

- `article p:first-child::first-line { }`

### ⭐**Descendant combinator**

- `li em {color: rebeccapurple;}`
  - To select only an `<em>` that is nested inside an `<li>` element

### ⭐ **Child combinator**

- `article > p { }`
  - selects only **the direct children**

### ⭐**Adjacent sibling combinator**

- `h1 + p {font-size: 200%;}`
  - styling a paragraph when it comes directly after a heading at the same hierarchy level

### ⭐ **General sibling combinator**

- `p ~ img`
  - select **siblings of an element even if they are not directly adjacent**

### 📌you can combine multiple selectors and combinators together

- `article p span {}`
  - `/* selects any <span> that is inside a <p>, which is inside an <article> */`
- `h1 + ul + p { }`
  - `/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1> */`

### 📌 Nesting to create complex selectors

- ![](z-Assets/Paste%20image%201695097054773image.png)
