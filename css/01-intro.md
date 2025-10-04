# What is CSS
- Cascading Style Sheets.
- Cascading means override/overlap the pre-built stylesheet of browser. Original is not deleted but your stylesheet has higher priority for same property and value. The original is always there for fallback.
- Specificity algorithm is basically more specifically targeted the element is the more weight will be give to that approach of target than other. 
    - High to low priority: Inline CSS > Id > Class > Tag/Element. 

# Basic structure
```css
selector {
    property: value;
}
```
# BEM model
- Block, Element, Modifier, is a widely used methodology for organizing CSS code. 
- It aims to improve code maintainability, reusability, and collaboration, especially in _larger projects_ and team environments.
- Syntax: `block--modifier` OR `block__element--modifier`
- Block: A standalone element, which is meaningful on its own. ex: card, button, menu.
- Element: A part of block that can't be used independently outside its parent block. ex: card__title, button__icon, menu__item.
- Modifier: A property to represent variable state of a block or element. ex: button--primary, card--disabled, menu__item--active.
- Encourages the use of class selectors and avoids deeply nested CSS, leading to lower and more manageable specificity.
```html
<div class="card card--featured">
  <h2 class="card__title">Product Title</h2>
  <p class="card__description">This is a description of the product.</p>
  <button class="card__button card__button--primary">Buy Now</button>
</div>
```
- Well you'll be using a framework which will generate classes and ids with its own naming convention in professional settings. So just read it.

# Tips
- View website left-to-right instead of top-to-bottom when deciding layout or CSS breakdown.
- Enforces you to see margins/width first (layout stuff) instead of focusing on content.

## Button Styles
- Must have styling for any button to get started.
```css
.button {
    padding: 5px 10px;
    border-radius: 5px;
    border: none;
    width: 200px; /*maybe*/
}
```

## Image Styles
- Must have styling for any image to get started.
```css
.image {
    object-fit: cover;
    border-radius: 20px;
    box-shadow: 0 0 10px #FFF;
    width: 100%;
}

.image:hover {
    transform: rotate(10deg);
    transition: all 0.5 ease-in-out;
}
```

## About Media Query
- Used to make responsive sites. For different screen sizes the layout and styling is decided again.
- Need to write different whole CSS multiple times for different screen sizes.
- Need to find range for mobile/small screen first.
- Don't bother with it. Use framworks and libraries.
- Anyways here's how you write one in pure CSS.
```css
@media media-type and (media-feature) {
  /* CSS rules to apply */
}
/* Media Type : all, screen, print, speech*/
/* Media Features : width, min-width, max-width, etc. */


@media screen and (max-width : 976px) {
    body {
        background-color: #1a1a;
    }
}
```
- (max-width: 768px) = Applying styles for screens smaller than 768px.
- (min-width: 600px) and (max-width: 1200px) = Applying styles for screens between 600px and 1200px wide.
- (min-width: 768px) = Applying styles for screens larger than 768px.
