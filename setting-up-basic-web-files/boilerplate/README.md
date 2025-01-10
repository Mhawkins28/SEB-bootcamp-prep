# HTML Boilerplate

Click on the `index.html` file created during setup and add HTML boilerplate by using Emmet, a powerful snippet tool that speeds up HTML and CSS workflow. Simply type `!` in the editor and then hit the `Tab` key, which will expand this shortcut into a full HTML template thanks to Emmet’s abbreviation expansion feature.

Let's review the boilerplate code generated!

## The HTML Boilerplate

Here’s an example of an HTML boilerplate. It should be inserted at the beginning of any HTML document to let browsers know that what follows is HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title> </title>
  </head>
  <body></body>
</html>
```

Let’s examine each of these lines more closely to find out what they do.

### The DOCTYPE tag

This lets your web browser know that the following document will be written in HTML.

```html
**<!DOCTYPE html>**
<html>
  <head>
    <title> </title>
  </head>

  <body></body>
</html>
```

### The html tag

The `<html>` tag begins your HTML document. It says, “Everything between my _opening_ tag (`<html>`) and my _closing_ tag (`</html>`) will be part of the following HTML-based instructions.”

```html
<!DOCTYPE html> **
<html>
  **
  <head>
    <title> </title>
  </head>
  <body></body>
  **
</html>
**
```

### The head tag

The `<head>` tag contains most of the under-the-hood stuff that helps identify your webpage and allows it to show up in search results. This is called **metadata**. It is also where you link any associated files - like the CSS and JS files.

```html
<!DOCTYPE html>
<html>
  **<head>
    **
    <title> </title>
    **</head
  >**

  <body></body>
</html>
```

### The title tag

The `<title>` tag may sound obvious, but in fact, it _doesn’t_ display any kind of title text on your webpage. Instead, the `<title>` tag provides your page with a name that will appear in search engine results. It’s also the text that appears at the top of your browser window or tab. See what appears for Netflix, Google, and Medium in the image below? Those are `<title>` tags in action. Feel free to type `My First Web App` for testing purposes.

```html
<!DOCTYPE html>
<html>
  <head>
    **
    <title>My First Web App</title>
    **
  </head>

  <body></body>
</html>
```

![link text](https://ga-instruction.s3.amazonaws.com/assets/intro-tech/html-unit-assets/intro-to-html/title%20tag.png)

### Linking CSS and JavaScript

To style your webpage, you'll need to link a CSS file to your HTML. Additionally, to add interactivity, you'll link a JavaScript file. Both files are linked in the `<head>` section of your HTML document.

1. **Linking the CSS file**: Below the `<title>` tag in the `<head>` section, use a `<link>` tag to link your CSS file named `main.css`, as follows:

   ```html
   <link rel="stylesheet" href="main.css" />
   ```

2. **Linking the JavaScript file**: Use a `<script>` tag to link your javascript file. To ensure that your JavaScript file, named `script.js`, doesn't block the HTML parsing while it loads, use the `defer` attribute. This attribute will execute the script after the HTML document has been fully parsed. Add the following line also within the `<head>` section, below the CSS link:

   ```html
   <script src="script.js" defer></script>
   ```

### The body tag

You’ll use the `<body>` tag to hold what’s actually displayed on your webpage, including all of your text, hyperlinks, and images. See the text and images that appear on Medium’s website? All of that is included in the `<body>`. Feel free to add an `<h1>` tag with the content `Hello World!`.

> Note: We will discuss how to display the HTML in the browser in the next lesson.

```html
<!DOCTYPE html>
<html>
  <head>
    <title> </title>
  </head>

  **
  <body>
    **
    <h1>Hello World!</h1>
    **
  </body>
  **
</html>
```

![link text](https://ga-instruction.s3.amazonaws.com/assets/intro-tech/html-unit-assets/intro-to-html/body%20tag.png)

Here is how your updated boilerplate should look:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web App</title>
    <link rel="stylesheet" href="main.css" />
    <script src="script.js" defer></script>
  </head>

  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

Now it's time to test in the browser!