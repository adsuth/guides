

# DOM 01 - Selectors

To manipulate the DOM, we first need a way to access its elements. This is done with **selectors**. 

You can select elements through any attribute they possess, but most commonly you’ll select them through their ID like so,

```javascript
const element = document.getElementById( "elementID" )
```

### Properties of Selected Elements

DOM elements have a lot of functionality baked in that we can use to do all sorts of things, from manipulating styles to adding event-based functionality.

You can access them like so:

```html
<p id="myElement"></p>
```

```javascript
const element = document.getElementById( "myElement" )

element.id // returns id of element, which is "myElement"

element.classList
```



We’ll touch on this more in the future, but for now its essential to realise that **DOM elements are objects** and as such, **DOM elements have methods and properties that we can access through dot notation.**

We can actually see the full list of methods and properties by using `console.dir()`,

```javascript
console.dir( element )
```

Now this will print out a daunting list of properties and methods, but we can ignore most of these as you’ll never really need them. There are only really a few things you‘ll need:

| Property / Method | What it Does                                                 | Element Types | Type   | Footnote |
| :---------------- | ------------------------------------------------------------ | ------------- | ------ | -------- |
| `style`           | Allows you to manipulate the style of an element             | All           | Object | [1]      |
| `innerText`       | Allows you to manipulate the text content of an element (eg: a `<p>`or `<h1>`). Safer than `innerHTML` | Text          | String |          |
| `innerHTML`       | Allows you to manipulate the children of an element          | Many          | String |          |
| `value`           | Access value of an `<input> `field                           | Input         | String |          |
| `className`       | Allows you to change or access class                         | All           | String |          |
| `classList`       | Allows you to add, remove or toggle classes on element       | All           | Object | [2]      |
|                   |                                                              |               |        |          |

