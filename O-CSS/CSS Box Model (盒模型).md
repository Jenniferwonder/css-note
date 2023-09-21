---
Title: CSS Box Model (盒模型) ^8d07e40e-395a-69d9
Type: D
tags:
  - CSS
status: 
DateStarted: 2023-09-20
DateModified: 2023-09-21
mindmap-plugin: basic
DateDone: 2023-09-20T00:00:00.000+08:00
---

# CSS Box Model (盒模型)

## Reference: https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model

## Block and Inline Boxes (Box Display Types)

### Outer display type ^720c783d-0ee8-f7be
- `display: block;`
    - The box will break onto a new line
    - The `width` and `height` properties are respected
    - `padding`, `margin` and `border` will cause other elements to be pushed away from the box
    - If `width` is not specified, the box will extend in the inline direction to fill the space available in its container.
        - In most cases, the box will become as wide as its container, filling up 100% of the space available.
    - 📌`<h1>` and `<p>`, use **block** as their outer display type by default
- `display: inline;`
    - The box will not break onto a new line
    - The `width` and `height` properties will not apply
    - Top and bottom padding, margins, and borders will apply but will **not cause** other inline boxes to move away from the box
    - Left and right padding, margins, and borders will apply and will **cause** other inline boxes to move away from the box.
        - ![[z-Assets/Paste image 1695105750202image.png]]
    - 📌 `<a>`, `<span>`, `<em>` and `<strong>` use **inline** as their outer display type by default
- `display: inline-block`
    - provides a middle ground
    - Use it if you do not want an item to break onto a new line, but do want it to respect width and height
        - ![[z-Assets/Paste image 1695105766252image.png]]
    - Allow padding to be set on it, making it easier for a user to click the link

### Inner display type ^62cc7bae-16a4-461e
- `flex`
- `grid`

## What is CSS Box Model?

### Parts of a box
- ![[z-Assets/Paste image 1695104770486image.png]]
- The margin is not counted towards the actual size of the box

### Margins, padding, and borders
- Margin collapsing
    - a thing that happens if you are creating space with margins and don't get the space you expect
- Borders
    - top, right, bottom, left
    - width, style, color
    - [[CSS Backgrounds and Borders]]

## What's the difference between Standard CSS Box Model and Alternative CSS Box Model? ^82ec8775-87e3-e6cd

### ⭐Standard CSS Box Model
- ![[z-Assets/Paste image 1695105117745image.png]]

### ⭐Alternative CSS Box Model
- `box-sizing: border-box`
    - ![[z-Assets/Paste image 1695105205521image.png]]
- 📌To use the alternative box model for all of your elements (which is a common choice among developers)

    -
      ```css
      html {
        box-sizing: border-box;
      }
      *,
      *::before,
      *::after {
        box-sizing: inherit;
      }
      ```