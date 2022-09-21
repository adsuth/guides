### JSON

**JSON** stands for JavaScript Object Notation. Its a file format used to store data. The file example is `.json`. As the name implies, its based on Javascript's syntax for defining objects, and as such is very similar albeit with a few key differences

```json
{
  "entry_1": {
    "key": "value"
  },
  "entry_2": {
    "key": [ 1, 2, 3 ]
  },
  "entry_3": {
    "key": {
      "innerKey": [ 1, 2, 3 ]
    }
  },
}
```

- JSON files must start and end with curly braces `{}`

- Keys must be in quotes

In node.js, you can import a local JSON file like so

```javascript
const data = require( "./jsonFileName.json" )

console.log( data ) // the json is already parsed, and ready to use as a JS object
```

### Getting Local JSON in The Browser

The easiest way to get local JSON in the browser is by using JQuery. Obviously, you'll need to setup JQuery in your project to do this first.

Once setup, you can get local JSON like so

```javascript
$.json( "./jsonFileName.json", data => {
  console.log( data )
} )

// alternatively, with more granular control
$.get({

})
```

Keep in mind **these methods are async by default**. So you'll need to cater your program accordingly.
