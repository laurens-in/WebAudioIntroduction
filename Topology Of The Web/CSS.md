CSS describes the **appearance** of a web-page.

Imagine that we have the following [[HTML]] structure:

```html
<div>
  <p id="first-paragraph" class="custom-text">Hello</p>
  <p id="second-paragraph" class="custom-text">World</p>
</div>
```

In our CSS style-sheet we have different selectors to identify these elements. Standard [[HTML]] elements can be accessed by using their tag name:

```css
div {
  background-color: #ffffff;
}
```

This will change the background color of all `<div>` elements.

We reference individual elements using their `id` attribute. We do this by using a `#` prefix:

```css
#first-paragraph {
  font-size: 20px;
}
```

This will change the font size of the element with `id="first-paragraph"`.

We reference multiple elements using their `class` attribute. We do this by using a `.` prefix:

```css
.custom-text {
  color: black;
}
```

This will change the text color of all elements with `class="custom-text"` to black.

There are many CSS properties, but we will not worry about them too much for now.

To link the CSS file inside your [[HTML]] file add the following line inside your `<head>` tag:

```html
<link rel="stylesheet" href="./path/to/file.css">
```
