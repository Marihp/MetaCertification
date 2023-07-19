# Javascript concepts

From Meta course, sheCodes bootcamp, and internet searches.

## Table of Contents

- [Variables](#variables)
- [Differences](#differences)
- [Data types](#data-types)
- [Operators](#operators)
  - [Arithmetic operators](#arithmetic-operators)
  - [Comparison operators](#comparison-operators)
  - [Logical operators](#logical-operators)
  - [Additional operators](#additional-operators)
- [Comments](#comments)
- [Additional resources](#additional-resources)
- [Conditionals](#conditionals)
  - [ELSE IF and SWITCH statements](#else-if-and-switch-statements)
  - [So what to use](#so-what-to-use)
- [Functions](#functions)
- [Arrays](#arrays)
- [Objects](#objects)
- [Selectors](#selectors)

## Variables

- **Key word**: `var`
- **Assignment operator**: `=`
- Variables can be reassigned, they are **not** immutable.

```javascript
var varName = "value";
console.log("Hello", varName);
```

### Differences

- `var`: global scope out of a function or local scope in a function, can be overwrite

```js
// El problema con var
var saludar = "hey, hola";
var tiempos = 4;

if (tiempos > 3) {
  var saludar = "dice Hola tambien";
}

console.log(saludar); // "dice Hola tambien"
```

- `let`: Should be preferred over var as it has block scope and solves the previous problem. Anything within curly braces is a block. Additionally, let variables can be modified but _not_ redeclared.

```js
let saludar = "dice Hola";
let tiempos = 4;

if (tiempos > 3) {
  let hola = "dice Hola tambien";
  console.log(hola); // "dice Hola tambien"
}
console.log(hola); // hola is not defined

let saludar = "dice Hola tambien"; // error: Identifier 'saludar' has already been declared
saludar = "dice hola tambien"; // Ok

// In block scope (no problem)
let saludar = "dice Hola";
if (true) {
  let saludar = "dice Hola tambien";
  console.log(saludar); // "dice Hola tambien"
}
console.log(saludar); // "dice Hola"
```

- `const`: Similar to let pero no puede modificarse ni volver a declararse.

## Data types

There are seven primitive data types in Javascript: String, Number, Boolean, Null, Undefined, BigInt and Symbol.

- **Number**: Floats and ints
- **String**: Text
- **Boolean**: Just True or False
- **Null**: The absence of a value
- **Undefined**: A variable not yet assigned a value
- **BigInt**: A data type that accommodates a greater range of numbers than number
- **Symbol**: A data type used as unique identifier

## Operators

Used to manipulate individual data items and return a result.

### Arithmetic operators

- **Power**: \*\*
- **Modulo**: %
  <img width="791" alt="Captura de pantalla 2023-06-13 a la(s) 9 56 26 a m" src="https://github.com/Marihp/MetaCertification/assets/111605652/5e959e49-b5bd-4b65-88a0-7cadcd6b53e6">

### Comparison operators

- Javascript only check if the values are equal, not the datatypes, so: `100 == "100" is true`, but `100 === "100" is false`, cause the `===` operator checks values and datatypes.
  <img width="1215" alt="Captura de pantalla 2023-06-13 a la(s) 9 55 32 a m" src="https://github.com/Marihp/MetaCertification/assets/111605652/29bbdd31-7883-4bfe-8abd-e6b0be0229ec">

### Logical Operators

<img width="783" alt="Captura de pantalla 2023-06-13 a la(s) 9 57 49 a m" src="https://github.com/Marihp/MetaCertification/assets/111605652/936b7303-a903-4dc0-a20a-40761aaedafb">

### Aditional Operators

- Logical **AND** operator: `&&`
- Logical **OR** operator: `||`
- Logical **NOT** operator: `!`
- **The modulus operator:** `%`
- **The equality operator:** `==`
- **The strict equality operator:** `===`
- **The inequality operator:** `!=`
- **The strict inequality operator:** `!==`
- \*\*The addition assignment operator: `+=`
- **The concatenation assignment operator:** `+=` (it's the same as the previous one)

> The diference with the stricts operators, is that the strict compare both values and datatypes.

## Comments

```js
// Single line comments

/*
   Multiline comments
*/
```

## Additional resources

- [Mozilla Developer Network Expressions and Operators
  ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)
- [Mozilla Developer Network Operator Precedence and Associativity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence) -[JavaScript Primitive Values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)
- [ECMA262 Specification](https://tc39.es/ecma262/)
- [jQuery Official Website](https://jquery.com/)
- [React official Website](https://reactjs.org/)
- [Emojis](http://unicode.org/emoji/charts/full-emoji-list.html#1f600)

## Conditionals

Handling multiple if and else staments.

### ELSE IF and SWITCH staments

```js
// Handling with else if
var place = "first"

if(place == "first"){
    console.log("Gold")
    }
else if (place == "second"){
   console.log("Silver")
   }
else if (place == "third"){
   console.log("Bronze")
   }
else {
    console.log("No medal")

// Handling with switch statement

switch(place) {
    case "first":
        console.log("Gold")
        break

    case "second":
        console.log("Silver")
        break

    case "third":
        console.log("Bronze")
        break

    default:
        console.log("No medal")
 }

```

### So what to use

Both if else and switch are used to determine the program execution flow based on whether or not some conditions have been met. There are referred to as **flow control statements**

- `if else`: is better suited if there is a binary choice in the condition.
- `switch`: If there are a lot of possible outcomes, it is best practice to use a switch statement because it is easier less verbose.

## Functions

For repetitive tasks, functions are a way to group a block of code and execute it whenever you want.

- Note: A function by default returns undefined.

```js
function nameFunction(arg_1, arg_2) {
  // Function body
  // Here goes the code
}
```

## Arrays

It´s like a train, remember that the indices begin in 0.

- Array Literal Syntax `[]`
- `["item 0", "item 1"]`
- Values in an array are all part of a group
- Values are set in a specific sequence
- Values can be accessde with their index

## Objects

It's the easiest way to operate "roles" in Javascript, objects can be described as collections of related properties where each property is represented as a key value pair.

```js
// Declare the object
var object = {
  atribute_1: 10,
  atribute_2: 23,
};

// Add new property
object.atr_3 = "Hello";
```

Cuando creo el objeto puedo seguir actualizandolo y añadiendo campos

## Selectors

Javascript can have access to all the HTML document with query, all the `document` and select specific classes

### Query selector

Returns the first element (if any) on the page matching the selector. `document.querySelector(whatIWantToSelect)`

```js
let li = document.querySelector("li");
let day = document.querySelector(".day");
let paragraph = document.querySelector("ul#list p");
```

### Query selector All

Returns all elements (if any) on the page matching the selector.

```js
let lis = document.querySelectorAll("li");
let paragraphs = document.querySelectorAll("li#special p");
```

### Creating an event listener

The sayHi function will be executed each time the city element is clicked.
Click is the most common event type but you can also use click | mouseenter | mouseleave | mousedown | mouseup | mousemove | keydown | keyup.

```js
function sayHi() {
  alert("hi");
}

let element = document.querySelector("#city");
element.addEventListener("click", sayHi);
```

### HTML content

Update the HTML content of the selected element.

```js
let li = document.querySelector("li");
li.innerHTML = "Hello World";
```

## Refactoring

Make the code more readable and code quality

### String concatenation

```js
let firstName = "Julie";
let lastName = "Johnson";
let fullName = firstName + " " + lastName; // "Julie Johnson"

// Better
let fullName = `${firstName} ${lastName}`;
```

### Template literals

```js
let city = "Denver";
let sentence = `Kate is from ${city}`; // Kate is from Denver
```

### JS Function Parameters

```js
function fullName(firstName, lastName) {
  alert(firstName + " " + lastName);
}

let firstName = prompt("What's your first name?");
let lastName = prompt("What's your last name?");
fullName(firstName, lastName);
fullName("Kate", "Robinson");
```

# For loops

Remember that an array is an Object

```js
for (var i = start; stop_condition; step (i++) {
    do this
}
```

# String cheat sheet

- charAt(): Find the character at this position
- concat(): concat strings
- indexOf(): search the index of the first match char
- lastIndexOf()
- split()
- toUpperCase()
- toLowerCase()

# Bugs and Errors

- Bug: A bug causes a program to run in an unintended way
- Error: An error causes a program to stop running

  ## Error types

  - Syntax Error: When you mis-type something
  - Type Error: When you try to do something that not match the type
  - Reference Error: Try to call something that have not been declared
  - Range Error: When you try to do something that is out of range

## Try and catch blocks

This guaranteed that your code still running after find an error

```js
try {
  // Code to try
} catch (error) {
  // Code to handle the error
  console.log(error);
}

// Example with throw new Error
function getRectArea(width, height) {
  if (isNaN(width) || isNaN(height)) {
    throw "Parameter is not a number!";
  }
}

try {
  getRectArea(3, "A");
} catch (e) {
  console.error(e);
  // expected output: "Parameter is not a number!"
}
```

## Types of empty values

- null: The absence of a value
- undefined: A variable not yet assigned a value
- NaN: Not a number

## Debugging



