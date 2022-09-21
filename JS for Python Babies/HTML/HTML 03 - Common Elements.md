# HTML 03 - Common Elements

HTML Documents are made up elements. Visible elements are stored in the `<body>` tag.

This page aims to serve as a list of all the major elements and their functions.

| Tag    | Example                     | Type      | Notes                                                                                 |
| ------ | --------------------------- | --------- | ------------------------------------------------------------------------------------- |
| h1     | `<h1>This is a Header</h1>` | Text      | Has multiple similar tags, 1 to 6.<br/>The higher the number, the smaller the header. |
| p      | `<p>a paragraph</p>`        | Text      | For a text paragraph                                                                  |
| b      | `<b>bold text</b>`          | Text      | Makes text bold                                                                       |
| i      | `<i>italic text</i>`        | Text      | Italicised text                                                                       |
|        |                             |           |                                                                                       |
| div    | `<div></div>`               | Container | Generic block container. Put stuff inside it to "group" together.                     |
| span   | `<span></span>`             | Container | Generic inline container. Put stuff inside it to "group" together.                    |
|        |                             |           |                                                                                       |
| input  | `<input type="text">`       | Input     | Multiple different `type` variations, see its own document.                           |
| button | `<button></button>`         | Input     |                                                                                       |

### Adding Style Through CSS

```html
<h1> This is a header </h1>
```

We can add style **to every tag of a certain type**:

```css
h1 {
  color: red;
}
```
