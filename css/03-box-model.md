# CSS Box Model & Box-Sizing

## 1. The CSS Box Model
- Every element in CSS is represented as a rectangular box.  
- The **box model** defines how the size of this box is calculated.

### Structure of the Box Model
1. **Content** → The actual text, image, or other content.
2. **Padding** → Space between content and the border (transparent area).
3. **Border** → The outline surrounding the padding and content.
4. **Margin** → Space outside the border; separates element from others.

## 2. box-sizing Property
- The `box-sizing` property defines how the browser calculates the width and height of an element. It determines whether padding and borders are included inside the declared width/height or added outside of it.

### Content-Box (default)
- In this mode, the width and height apply only to the content area. Padding and borders are added on top of that, which increases the final size of the element.

Example:
```css
box-sizing: content-box;
width: 200px;
padding: 20px;
border: 5px solid;
```
- Here, the total width becomes 200px (content) + 20px left padding + 20px right padding + 5px left border + 5px right border = 250px.

### Border-Box
- In this mode, the width and height include the content, padding, and border. This means the declared size is the final size of the element, and the content area shrinks to make room for padding and border.

Example:
```css
box-sizing: border-box;
width: 200px;
padding: 20px;
border: 5px solid;
```
- Here, the total width stays 200px. The content area reduces in size so that padding and borders fit inside the defined width.

### Best practice
- Since border-box makes layout calculations easier and more predictable, it is often set as a global default in projects
```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```