# Java S - Working With Strings

Strings are essentially **arrays of characters**. They are perhaps the most unique of the common data types you'll be working with. They are not primitive, and have a few methods and properties to play with.

##### String Methods

*In the below examples, `String str = "Hello World!";`*

| Method        | Example                             | Output            | What it Does                                                                                                                 |
| ------------- | ----------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| charAt()      | `str.charAt( 0 )`                   | `'H'`             | returns the **char** at given position (not String)                                                                          |
| contains()    | `str.contains( "Hello" )`           | `true`            | checks if given sequence is in string                                                                                        |
| endsWith()    | `str.endsWith( "!" )`               | `true`            | checks if the string ends with given string (useful for checking file extensions)                                            |
| startsWith()  | `str.startsWith( "Hello" )`         | `true`            | checks if the string starts with given string (useful for checking for file prefixes)                                        |
| equals()      | `str.equals( "Hello World!" )`      | `true`            | checks if two strings are equal [1]                                                                                          |
| indexOf()     | `str.indexOf( "l" )`                | `2`               | finds **first** index of given String (can be multiple characters eg: "Hello" would return 0)                                |
| lastIndexOf() | `str.lastIndexOf( "l" )`            | `9`               | finds **last** index of given String (can be multiple characters eg: "Hello" would return 0)                                 |
| length()      | `str.length()`                      | `12`              | returns the length of the string                                                                                             |
| replace()     | `str.replace( "Hello", "Goodbye" )` | `"Goodbye World"` | replaces first string argument with last string argument (replaces **all occurences**). Does nothing if target doesnt exist. |
| split()       | `"1,2,3".split(",")`                | `["1","2","3"]`   | splits the string by the given delimiter, and creates an array of substrings                                                 |
| substring()   | `str.substring(0, 5)`               | `"Hello"`         | Returns a new string with characters from first position to last position (excl. last character)                             |
| toCharArray() | "abc".toCharArray()                 | `['a','b','c']`   | Returns a character array with each character in the string                                                                  |
| toUpperCase() | `str.toUpperCase()`                 | `"HELLO WORLD!"`  | Capitalises each character in the string                                                                                     |
| toLowerCase() | `str.toLowerCase()`                 | `hello world!`    | Lower cases each character in the string                                                                                     |
| trim()        | `"   hello there     ".trim()`      | `"hello there"`   | removes spaces from beginning and end of string                                                                              |


