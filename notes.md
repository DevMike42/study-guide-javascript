# JavaScript

## Basic JavaScript

### **Comments**
* Comments are lines of code that are intentionally ignored
* They are a way of providing notes for yourself or whoever has to read and understand your code
* `//` is used to comment out a single line of code
* Multiple lines of code can be commented out by using wrapping the code in a beginning `/*` and ending `*/`
```js
// This is a single-line comment

/* This is a 
multi-line comment */
```

### **Variables**

#### **Declaring Variables**
* Allow computers to store and manipulate data
* Variables use a "label" to point to the data rather than pointing to the data itself
* Data types
    * Number - An actual number value (ex. 12)
    * String - A collection of characters. Written within `""` or `''`. (ex. "dog")
    * Boolean - A true or false value (ex. true)
    * Object - A collection of other data types 
    * Undefined
    * Null
    * Symbol
* Variables are created or "declared" by putting the word `var` in front of the data "label"
* Variable names or "labels" may contain letters, numbers, and `$`, or `_` but may not start with a number
```js
var myName;
```

#### **Storing values with the Assignment Operator**
* Values are assigned to a variable using `=` as the Assignment Operator
* The label is on the left of the `=`, the value goes on the right followed by a `;` as a closing tag
```js
var myName = "Mike";
var favNum = 45;
```
* Values for variables can be re-assigned as shown below
```js
// The variable is declared
var a;
// A value of 5 is assigned 
a = 5;
// A new value of 10 is assigned 
a = 10;
```
* Initializing a variable is when a variable is declared and at the same time it is assigned a value
```js
var x = 10;
``` 