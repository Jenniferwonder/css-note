---
Title: CSS Values and Units
Type: D
tags:
  - CSS
status: 
DateStarted: 2023-09-20
DateModified: 2023-09-21
mindmap-plugin: basic
DateDone: 2023-09-20T00:00:00.000+08:00
---
### CSS Values and Units
- What is a CSS value?
    - A value type in CSS is a way to define a collection of allowable values.
- Numbers, lengths and percentages
    - Numeric value types
        - ![[O-CSS-Numeric value types.png|500]]
    - Lengths
        - Absolute length units
            - ![[z-Assets/Paste image 1695215128544image.png]]
        - Relative length units
            - ![[z-Assets/Paste image 1695215216372image.png]]
    - Percentages
        - always set relative to its parent's value
    - Numbers
        - `opacity`
            - `0`
                - fully transparent
            - `1`
                - fully opaque
- Color
    - Color keywords
    - Hexadecimal RGB values
    - RGB and RGBA values
    - HSL and HSLA values
- Images
    - actual image file pointed to via a url() function
    - a gradient
- Position
    - a set of 2D coordinates
    - two values — the first sets the position **horizontally**, the second **vertically**
    - `background-position: right 40px;`
        - positioned a background image 40px from the top and to the right of the container using a keyword
        - ![[z-Assets/Paste image 1695216235183image.png]]
- Strings and Identifiers
    - identifiers (keywords)
        - a special value CSS understands
    - strings
        - quoted to demonstrate generated content
        - `content: "This is a string."`
- Functions