# Algorithm Scripting

## Overview
A computer algorithm is a sequence of steps that is followed to achieve a particular outcome. The best practice is to break a problem down into chunks and solve each chunk one at a time. 

## Examples

1. ### Convert Celcius to Fahrenhit

```js
function convertToF(celsius) {
  let fahrenheit;
  fahrenheit = celsius * 9/5 + 32;
  console.log("Fahrenheit converted = " + fahrenheit);
}

convertToF(30);

// Output - Fahrenheit converted = 86
```

2. ### Reverse a String

```js
function reverseString(str) {
  return str.split('').reverse('').join('');
}

reverseString("hello");

// Output - "olleh"
```
Explanation
* First step is to convert the string to an array of characters using the `.split` method.
* Next, we __*chain*__ the `.reverse` method to reverse the order of the characters.
* Finally, we __*chain*__ the `.join` method to join the characters back together in the form of a string.