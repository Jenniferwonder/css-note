---
DateDue: 
Title: "CSS Motion "
Type: D
tags:
  - CSS
DateStarted: 2024-01-12
DateModified: 2024-01-12
DateDo: 
DateDone: 2024-01-19T00:00:00.000+08:00
status: 
mindmap-plugin: basic
Topic: Motion
Difficulty: Hard
---

# CSS Animation & Transition

## 📌[S-CSS Animation](S-CSS%20Animation.md)

## `transition`

### 💡a way of animating an element from one state to another

### `transition: filter 300ms`

### `transition-property`
- `none`
- `all`
- `color`
- `background-color/ border-color/ text-decoration-color`
- `opacity`
- `box-shadow`
- `transform`

### `transition-timing-function`

### `transition-duration`

### A multistage transition
- `transition: background-color 500ms,
                   transform 500ms 500ms;`

### 📌Properties that supports transition
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

## 🏷️[CSS Transform](CSS%20Transform.md)

## `@keyframes`

### `@keyframes logo-spin {from {transform: rotate(0deg)} to {transform: rotate(360deg)}}`
- 🏷️[CSS Transform](CSS%20Transform.md)

### `@keyframes colors {0% { } 50% { } 100%{ }}`

## `animation`

### `animation: logo-spin infinite 20s linear`
- The first time value encountered is treated as the `duration`, and the second is treated as the `delay`

### `animation-name`

### `animation-duration`

### `animation-timing-function`
- `cubic-bezier(.17, .67, .9, .6);`
    - `linear`
    - `ease`
    - `ease-in`
    - `ease-out`
    - `ease-in-out`
    - Resources for cubic-bezier
        - https://matthewlein.com/tools/ceaser
        - https://cubic-bezier.com
- `steps(step-count, direction)`

### `animation-delay`

### `animation-fill-mode`
- `none`
- `forwards`
- `backwards`
- `both`

### `animation-iteration-count`
- `infinite`

### `animation-direction`
- `normal`
- `reverse`
- `alternate`
- `alternate-reverse`

### `animation-play-state`
- `running`
- `paused`
- could be manipulated with JavaScript to pause and resume an animation

### Multiple animations
- supports a comma-separated list of multiple values
- `animation: color 5s alternate infinite,
                    spin 1s linear infinite;`

## Performance

### `will-change: filter`
- a hint for the browser about which property/ properties will change
- Overuse would impact performance

### avoid animating layout properties, as these can negatively affect performance

## Accessibility

### `@media(prefers-reduced-motion: no-preference)`

### `@media (prefers-reduced-motion: reduce) {
- not supported in internet explorer