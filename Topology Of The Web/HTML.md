Defines the **structure** of the web-page. Is an XML based markup language that contains semantic elements to describe the document tree:

```html
<body>
  <main>
    <!--This is a comment. Comments are not displayed in the browser-->
    <h1 id="title">Hello World<h1>
    <p class="some-text">HTML is pretty simple</p>
  </main>
</body>
```

An element normally contains an opening and a closing tag, for example:

```html
<p> <!-- opening tag -->
  Hello world!
</p> <!-- closing tag -->
```

Elements can have named attributes, for example:

```html
<div id="random-image" class="image-container">
  <img src="https://picsum.photos/200"> 
</div>  
```

The most important attributes are `id` and `class` and every element can use them. They are used to identify specific elements from [[CSS]] or [[JavaScript]]. An `id` is unique and used to reference one element, `class` is used for shared styles or behaviors.

Since the `<img>` element can contain no children, it doesn't need a closing tag. Such elements are called [void elements](https://developer.mozilla.org/en-US/docs/Glossary/Void_element).

This [list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) contains all HTML elements. Often we also need a generic element to implement custom functionality, in most cases we use a `<div>` element for this. Whenever there is a semantic element available it should be preferred to a `<div>`.

Every HTML file must contain at least the following boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>name of your site<title>
    <!-- the following line links the style.css file -->
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
  <!-- inside the body element you can define the html structure of your page -->
  <!-- the following line links the index.js file -->
	<script src="index.js"></script>
  </body>
</html>
```

The `<head>` element contains some metadata about our page, you don't need to worry about this for now.
