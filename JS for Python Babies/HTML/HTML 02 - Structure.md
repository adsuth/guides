# HTML 02 - Structure

HTML has a lot of boilerplate, but luckily Emmet, an integrated extension, can generate most of for you.

Typing `!` and hitting tab will generate the following:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

You can ignore most of this for now, just know it's all needed. What you should take note of is the `<head>` and `<body>`.

### The Head

This is where your **metadata** is stored; links to stylesheets, favicon and other meta tags like the title of the page - what is shown on the tab.

##### Linking Style Sheets

You can link styles with the following:

```html
<link rel="stylesheet" href="./pathToCSS.css">
```

##### Linking Scripts

Traditionally, your `<script>` tags should be at the bottom of the body - this is because the HTML is loaded sequentially, and so you need to make sure every other tag that may be manipulated by the script is loaded before.

However, with the `defer` attribute, we can put our tags in the `<head>` to keep everything together. 

`defer` ensures the scripts are staggered until the **entire document is loaded**.

You can link scripts with the following:

```html
<script src="./pathToScript.js" defer></script>
```

### The Body

The body is where all your *visible* content is stored. Headers, text, buttons, etc.

We'll touch on this in later pages.
