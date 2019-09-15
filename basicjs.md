# Basic JavaScript

## **Comments**
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

## **Variables**

### **Declaring Variables**
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

### **Storing values with the Assignment Operator**
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

### **Understanding Uninitialized Variables** ####
* When a variable is declared and not initialized with a value it has a initial value of `undefined`
* A mathematical operation that includes and undefined variable will return `NAN` (No A Number)
* If you concatenate a string with an undefined variable it will return a string of "undefined"

-------------------------------------------------------------------------------

## **JavaScript Operators**

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

## **Strings**

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

3. __Escape Sequences__ - Gives you the ability to add certain characters and formatting to a string that you would not normally be able to type out. (ex. a backslash, tab, or newline, etc.)

    * `\'` - Single quote
    * `\'` - Double quote
    * `\\` - Backslash
    * `\n` - New Line
    * `\r` - Carriage return
    * `\t` - Tab
    * `\b` - Backspace
    * `\f` - Form feed

    ```js
    var myString = "FirstLine\n\t\bSecondLine\nThirdline";

    /* Output 
    FirstLine
        \SecondLine
    Thirdline
    */
    ```

4. __Concatenating Strings using the Plus Operator__ - Build new strings out of other strings by concatentating them together.

```js
var myString = "This is the start. " + "This is the end";

// Output - This is the start. This is the end.
```

5. __Concatentating Strings using the += Operator__ - The += operator concatenates one string onto the end of another.

```js
var myString = "This is the first sentence. ";
myString += "This is the second sentence.";

// Output - This is the first sentence. This is the second sentence.
```

5. __Find the length of a String__ - The `.length` property will give you the number of characters in a String.

```js
var myString = "Michael";
var myStrLength = myString.length;
console.log(myStrLength);

// Output - 7
```

6. __Bracket Notation__ - Bracket notation is used to find the value of a specific character within a String or Array. The first character will be located at `[0]`

Finding the `Nth` letter in a String
```js
var myStr = "ABCDEFG";
firstLetterOfMyStr = myStr[0]; // Output - A
thirdLetterOfMyStr = mystr[2]; // Output - C
```

Finding the `last` letter in a String
```js
var myName = "Michael";
lastLetterOfMyName = myName[myName.length -1];
// .length = 7
// 7 - 1 = 6
// The last character in myName is located at myName[6]
```

Finding the `Nth-to-last` letter in a String
```js
var myName = "Michael";
var secondToLastLetterOfMyName = myName[myName.length -2]; // Output - e
var thirdToLastLetterOfMyName = myName[myName.length -3]; // Output - a
```

7. __String Immutability__ - Within a String, values are ***immutable*** which means they cannot be changed. The entire value of a String can be changed but the characters alone cannot.

```js
var myStr = "Bob";
myStr[0] = "J"; // Will not work

myStr = "Job"; // The correct solution
```

