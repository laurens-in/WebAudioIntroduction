---
title: Your First Website
---

As an exercise we are going to create a website "from the ground up".

Create a folder for your website and inside it create an `index.html` file. This is usually the entry-point to your website and most [[Web Server]]s will automatically detect it as such.

First there is some [boilerplate code](https://en.wikipedia.org/wiki/Boilerplate_code) that we have to take care of. Copy this [[HTML]]-snippet into your `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My first website</title>
  </head>
  <body>
    <h1>Hello world!</h1>
  </body>
</html>
```

> [!info]
> If you want to, you can now start your `dev server` inside this folder and reload the page after each step to see it's impact.

This contains some info about our page as well as its content, don't worry too much about all this for now - what's important for us is the `<body>` element, our content will go here.

As a next step we are going to add a [[CSS]] file to apply some styles to our page. Create a file called `style.css` and add the following code to it:

```css
h1 {
  color: rgb(130, 15, 20);
}
```

Here we till the browser to render all `<h1>` elements with a text color of `fuchsia`. If we were to open our page now we would see that the color didn't change, this is because the browser doesn't know about our `style.css` file yet. When we request the page on a server it will give us back the `index.html` file, but the `index.html` file doesn't contain any reference to our style file, so our browser doesn't know that it needs to fetch this file too.

To change this we add the following line to our `index.html`, inside the `<head>` element:

```html
<link rel="stylesheet" href="style.css">
```

Now our browser will know that we have linked a style-sheet and that it needs to fetch it from the server and apply the styles. If we were to reload our page now, the styles would be applied.

So far everything on our page is completely static. If we want to make it interactive or dynamic we need to add some [[JavaScript]]. First we need an element that we want to interact with. Add the following line to your `index.html` file inside the `<body>` element below the `<h1>` element:

```html
<button id="my-button">Click me!</button>
```

Now create a `main.js` file and link it inside the `index.html` file inside the `<body>` element like this:

```html
<script type="module" src="main.js"></script>
```

> [!warning] Careful
> You should put all your script tags at the end of the body element to make sure everything else is already rendered when our [[JavaScript]] is loaded.

Now we get to the interesting part. First we need to get a reference to our `<button>` element. Paste the following line at the top of your `main.js` file:

```js
const button = document.querySelector("#my-button");
```

> [!info]
> `document.querySelector` allows us to use [[CSS]]-style queries to select elements from our html. The [[CSS]] selector for `id` is `#`, that's why we use `#my-button` to reference our `<button>` element

Now that we have a reference to our `<button>` we can attach a function to it that will be triggered when the button receives a click event. To do so, we first define our function:

```js
function handleClick() {
  console.log("Hello world!")
}
```

This simply outputs the string `"Hello world!"` to the developer console whenever the button is pressed.

>[!info]
>To open the developer console press <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd> (Windows/Linux) or <kbd>⌘</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd> (macOS) and navigate to the console tab.

Now to bring it all together we attach an event listener to the button that triggers our function:

```js
button.addEventListener("click", handleClick)
```

Now reload the page, press the button and see what happens!
