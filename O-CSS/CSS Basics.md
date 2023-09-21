---
Title: CSS Basics
Type: D
tags: 
status: 
DateStarted: 2023-09-18T00:00:00.000+08:00
DateModified: 2023-09-21
mindmap-plugin: basic
DateDone: 2023-09-18T00:00:00.000+08:00
---

# CSS Basics

## 全称

### 层叠样式表 (Cascading Style Sheets)

### 一种样式表语言，用来描述 HTML 或 XML（包括如 SVG、MathML 或 XHTML 之类的 XML 分支语言）文档的呈现方式

## Apply CSS to HTML

### External stylesheet
- You can link a single CSS file to multiple web pages, styling all of them with the same CSS stylesheet
- `<link rel="stylesheet" href="styles.css" />`

### Internal stylesheet
- `<style></style>`
- internal stylesheets can be useful: when you're working with a content management system where you are blocked from modifying external CSS files

### Inline styles
- `<p style="color:red;">This is my first CSS example</p>`
- Avoid using CSS in this way, when possible
    - One styling change might require multiple edits within a single web page
    - making everything more difficult to read and understand

## Comments

### This helps to navigate the codebase as it gets larger

## White space

### can improve readability

### separate distinct values from one another by at least one space

## How CSS works?

### ❓What happens when a browser loads a webpage ^33dcf977-14ca-57a2
- The browser parses the fetched CSS, and sorts the different rules by their selector types into different "buckets", e.g. element, class, ID, and so on. Based on the selectors it finds, it works out which rules should be applied to which nodes in the DOM, and attaches style to them as required (this intermediate step is called a render tree)
- ![[O-CSS-Browser loads webpage.png]]

### ❓What happens if a browser encounters CSS it doesn't understand? ^a07d7472-a8d6-6940
- it does nothing, and just moves on to the next bit of CSS
- This enables basic fallback styling.
    - It means that you can use new CSS as an enhancement
