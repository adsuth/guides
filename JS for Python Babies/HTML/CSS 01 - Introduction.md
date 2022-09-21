# CSS 01 - Introduction

**CSS** stands for **Cascading Stylesheets**, and are a way of applying styles to your HTML documents through adding styling rules to selectors.

A selector can be a variety of things, from the name of a tag, a class name, an ID and even certain events like hovering and on focus. You can also select neighboring tags, child elements and so forth.

Every HTML tag **[has default styling](https://www.w3schools.com/cssref/css_default_values.asp)** already applied, but we can override them by adding our own CSS.

### Inline, Internal and External Styling

##### Inline

Inline styling refers to styling applied **within the tag itself**. It is not recommended due to how difficult it is to maintain, but you can do it like so:

```html
<h1 style="color: red;"></h1>
```

The `style` attribute allows you to write a CSS string that will apply the styles to **that element, and that element alone**.

##### Internal

Internal Styling refers to styling written within a `<style>` tag. The `<style>` tag is an HTML tag that will act as a micro-environment for writing CSS. Its styles will be applied across **only the page its on**. That's its limitation: It isn't portable, and only serves to make the HTML more messy. It's preferable to separate your HTML, JS and CSS.

##### External

External Styling refers to styling by using `.css` files - which you can then link in the `<head>` (see how to link CSS here). This is by far the most preferable way to go about styling your documents, and one CSS file can even be used across multiple HTML pages.

### Recommended: SASS

SASS stands for Syntactically Awesome Stylesheets. It's a more modern way of writing CSS, with a lot of neat features over plain old CSS - the best one being **the ability to nest selectors**.

For example, if I wanted to change the color of `<h1>` tags, but only if they are within a `<div>`, I can do so like this in SASS:

```scss
div {
  // div styles here
  h1 {
    color: red;
  }
}
```

In plain CSS, its a little more convoluted and messy

```css
div > h1 {
  color: red;
}
div {
  /* div styles here */
}
```

You'd need a new rule for `div`, `h1`.

SASS also supports `// inline comments`, something that CSS just doesn't for some reason.

##### Download the SASS Live Compiler Extension

You need to compile your SASS every time you make a change, but with this extension, it'll automatically do that for you every time you save your SASS file. **Just make sure you are watching your SASS**.

##### SASS vs SCSS

There are a few difference between `.scss` and `.sass` files. I personally prefer the former, and **its what I'd recommend due to how similar it is to CSS**. You'll learn CSS and SCSS at the same time, rather than one or the other. The main difference is syntax:

In SASS

```sass
h1
  color: red
  span
    color: blue
```

In SCSS

```scss
h1 {
  color: red;
  span {
    color: blue;
  }
}
```
