1. **Inline**
- To apply css for a single element.
- use `style` attribute.
```html
<h1 style="color:blue;">A Blue Heading</h1>
```

2. **Internal**
- To define styles for single page.
- use `<style>` tag.
```html
<style>
    body {
        background-color: powderblue;
    }
    h1 {
        color: blue;
    }
    p {
        color: red;
    }
</style>
```

3. **External**
- To define styles in seperate files to be used in any page.
- use `filename.css` and link it to html file using `<link>` tag inside `<head>` tag.
```html
<head>
    <link rel="stylesheet" href="filename.css">
</head>
```