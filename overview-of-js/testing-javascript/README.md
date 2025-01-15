# Testing JavaScript

## Introduction

Testing your JavaScript code is crucial to ensure it performs as expected. In this lesson, we will explore three different ways to test JavaScript code: running a JavaScript file in the terminal using Node.js, linking a JavaScript file to an HTML file and observing outputs in the browser console, and using an online IDE like CodePen.

## Testing with Node.js

### Steps

1. **Create a JavaScript file**: Name it `example.js`.

   ```bash
   touch example.js
   ```

2. **Write some code**: Open `example.js` in your text editor and write some basic JavaScript. For example:

   ```javascript
   console.log("Hello, world!");
   ```

3. **Run your script**: Open your terminal, navigate to the directory containing `example.js`, and run:

   ```bash
   node example.js
   ```

4. **Check the output**: You should see `"Hello, world!"` printed in the terminal.

## Testing in the Browser

### Steps

For a deeper explanation of this section, check out the boiler-plate lessons.

1. **Create an HTML and JavaScript file**: Name them index.html and script.js respectively.

2. **Link JavaScript to HTML**: Add the following code to index.html:

   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <title>Test JS</title>
       <script src="script.js" defer></script>
     </head>
     <body></body>
   </html>
   ```

3. **Write some JavaScript**: Open script.js and add:

   ```javascript
   console.log("JavaScript is linked and running!");
   ```

4. **Open in a browser**: Open `index.html` in a browser.

5. **Open Developer Tools**: Right-click on the page, select 'Inspect' or 'Inspect Element', and navigate to the 'Console' tab to see your JavaScript output.

## Testing in Alternate IDE (Codepen)

Testing your JS in CodePen will differ somewhat from running JS in a browser or a terminal.

## Steps

1. **Go to [CodePen](https://codepen.io/)**: Create a new pen.

2. **Write JavaScript**: In the JS panel, add some code like:

   ```javascript
   console.log("Testing in CodePen!");
   ```

3. **Open the Console**: Click the 'console' button at the bottom left area of your browser in CodePen to view logs.

## Conclusion

You've now learned three different ways to test your JavaScript code. Each method is useful depending on the context and the type of testing you need to do. Experiment with each to get comfortable with how they work - pick whichever environment you prefer to work in.

> Note: `console.log()` is a `function` used to print information to the console; more on `functions` in a future lesson.
