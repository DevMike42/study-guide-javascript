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

-------------------------------------------------------------------------------

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

#### **Understanding Uninitialized Variables** ####
* When a variable is declared and not initialized with a value it has a initial value of `undefined`
* A mathematical operation that includes and undefined variable will return `NAN` (No A Number)
* If you concatenate a string with an undefined variable it will return a string of "undefined"

-------------------------------------------------------------------------------

### **JavaScript Operators**

1. __Arithmetic Operators__
    * (`+`) Add operator. Adds 2 numbers or concatenates 2 variables
    ```js
    var num1 = 5;
    var num2 = 10;
    var sum = num1 + num2;
    // Output of sum will be 15
    var string1 = "one";
    var string2 = "two";
    var concat = string1 + string2;
    // Output of concat will be "onetwo"
    var example = string1 + num1;
    // Output of example will be "one5"
    ```
    * (`-`) Subtract operator. Acts the same as the addition operator. The only difference is it will only work with numbers. If one variable is not a number it will return `NaN`
    * (`*`) Mulitply operator. Same rules as subtraction.
    * (`/`) Divide operator. 
    * (`++`) Increment operator. Increments a number by 1.
    ```js
    var i = 1;
    i++;
    // Output will be 2
    i + 1;
    // Same as i++
    ```
    * (`--`) Decrement operator. Decrements a number by 1.
    ```js
    var i = 10;
    i--;
    // Output wil be 9
    i - 1;
    // Same as i--
    ```
    * (`%`) Remainder operator. Gives the remainder of the divison of 2 numbers.
    ```js
    var remainder = 5 % 2;
    // Output is 1
    // Output will only be the remainder portion of 5 divided by 2
    ```
    _The remainder operator can also be used to determine if a number is even or odd_
    ```
    17 % 2 = 1 (17 is Odd)
    48 % 2 = 0 (48 is Even)
    ```
    _The remainder operator is sometimes incorrectly referred to as the "modulus" operator. It is very similar to modulus, but does not work properly with negative numbers._


2. __Assignment Operators__ - Assignment operators are used to assign values to JavaScript variables
    * (`+=`) Will add the value to the right of the operator to the variable
    ```
    ex. (x += y) is the same as (x = x + y)
    ```
    ```js
    var myVar = 1;
    myVar += 5;
    console.log(myVar); // Returns 6
    ```
    * (`-=`) Will subtract the value to the right of the operator to the variable
    ```
    ex. (x -= y) is the same as (x = x - y)
    ```
    ```js
    var myVar = 6;
    myVar -= 5;
    console.log(myVar); // Returns 1
    ```
    * (`*=`) Multiplies a variable by a number
    ```
    ex. (x *= y) is the same as (x = x * y)
    ```
    ```js
    var myVar = 5;
    myVar *= 5;
    console.log(myVar); // Returns 25
    ```
    * (`/=`) Divides a variable by a number
    ```
    ex. (x /= y) is the same as (x = x / y)
    ```
    ```js
    var myVar = 25;
    myVar /= 5;
    console.log(myVar); // Returns 5
    ```
    * (`%/`) Finds the remainder of a variable when divided by a number
    ```
    ex. (x %= y) is the same as (x = x % y)
    ```
    ```js
    var myVar = 5;
    myVar %= 2;
    console.log(myVar); // Returns 1
    ```

-------------------------------------------------------------------------------

### **Strings**

1. __Literal Quotes within Strings__ - To insert literal quotes within the quotes of a defined string, use `\` in front of the starting and ending quotes.
```js
var myString = "I am a \"quote within\" a string.";
```
```
Output = I am a "quote within" a string.
```

2. __Using Single Quotes in Strings__ - Single or Double quotes function the same individually. Single quotes can be used if for example defining an `<a>` tag with attributes.
```js
var myTag = '<a href="http://www.example.com" target="_blank">Link</a>';
```
```
Output = <a href="http://www.example.com" target="_blank">Link</a>
```

