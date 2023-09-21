---
Title: CSS Backgrounds and Borders
Type: D
tags:
  - CSS
status: 
DateStarted: 2023-09-20T00:00:00.000+08:00
DateModified: 2023-09-21
mindmap-plugin: basic
DateDone: 2023-09-20T00:00:00.000+08:00
---

# [[O-CSS|CSS]] Backgrounds and Borders

## Backgrounds

### Shorthand Property & Values
- `background: url(bg-graphic.png) 10px 10px repeat-x fixed, red;`

    -
      ```css
      background-color: red;
      background-image: url(bg-graphic.png);
      background-position: 10px 10px;
      background-repeat: repeat-x;
      background-attachment: fixed;
      ```

- A background-color may only be specified **after the final comma**
- The value of `background-size` may only be included immediately after **`background-position`**, separated with the '/' character, like this: center/80%

### `background-image`
- Multiple background images
    - Each value of the different properties will match up to the values in the same position in the other properties.
- ⭐Gradient backgrounds
    - `linear-gradient (to left, color 1, color 2)`
    - `radial-gradient(circle, rgba(0,249,255,1) 39%, rgba(51,56,57,1) 96%)`
    - 📌[Gradient Generator](https://cssgradient.io/)

### `background-repeat`
- `no-repeat`
    - stop the background from repeating altogether.
- `repeat-x`
    - repeat horizontally
- ``repeat-y``
    - repeat vertically
- `repeat`
    - the default; repeat in both directions

### `background-position`
- uses a coordinate system in which the **top-left-hand corner** of the box is (0,0)
- 2 value
    - horizontal, vertical
        - `background-position: top center;`
        - `background-position: 20px 10%;`
        - `background-position: 20px top;`
- 4 value
    - indicate a distance from certain edges of the box
    - 📌positioning the background 20px from the top and 10px from the right
        - `background-position: top 20px right 10px;`

### `background-size`
- `cover`
    - make the image just large enough so that it completely covers the box area while still retaining its aspect ratio
    - 📌part of the image may end up outside the box
- `contain`
    - make the image the right size to fit inside the box
    - 📌may end up with gaps on either side
- length or percentage value
    - `background-size: 100px 10em;`

### `background-attachment`
- `scroll`
    - causes the element's background to **scroll when the page is scrolled**
- `fixed`
    - causes an element's background to **be fixed to the viewport**
- `local`
    - fixes the background to **the element it is set on**
- 📌 [Demo](https://mdn.github.io/learning-area/css/styling-boxes/backgrounds/background-attachment.html)

### `background-color`

### 📌Accessibility consideration
- Any important content should be part of the HTML page and not contained in a background.

## Borders

### Shorthand Property & Values
- `border: width, style, color;`
- top, right, bottom, left...

### Rounded Corners (圆角)
- `border-radius`
    - the first value defining the **horizontal radius**, and the second the **vertical radius**
    - pass in one value, which will be used for **both horizontal and vertical radius**.
    - | [Fancy Border Radius](https://9elements.github.io/fancy-border-radius/full-control.html)| Eight values specifying border-radius in CSS ( border-radius generator ) |

### 阴影-box-shadow
- [CSS box-shadow](https://getcssscan.com/css-box-shadow-examples) | 91 Beautiful CSS box-shadow examples. |
- [Shadow Palette Generator](https://www.joshwcomeau.com/shadow-palette/)| Create a set of lush, realistic CSS shadows.
- [CSS Shadow Gradients](https://alvarotrigo.com/shadow-gradients/) | Generate CSS Gradients For Shadows. |

### [[CSS Box Model (盒模型)]]