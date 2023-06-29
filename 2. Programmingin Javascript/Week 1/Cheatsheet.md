# Javascript concepts

## Variables
- **Key word**: var
- **Assignment operator:** =
- Las variables se pueden reasignar, **no** son inmutables.
```js
var varName = "value"
console.log("Hello", varName)
```

## Data types
There are seven primitive data types in Javascript: String, Number, Boolean, Null, Undefined, BigInt and Symbol.

- **Number**: Floats and ints
- **String**: Text
- **Boolean**: Just True or False
- **Null**: The absence of a value
- **Undefined**: A variable not yet assigned a value
- **BigInt**:  A data type that accommodates a greater range of numbers than number
- **Symbol**: A data type used as unique identifier

## Operators
Used to manipulate individual data items and return a result.

### Arithmetic operators
- **Power**: \**
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
  - **The addition assignment operator: `+=`
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
- [Mozilla Developer Network Operator Precedence and Associativity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
-[JavaScript Primitive Values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)
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
For repetitive tasks
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
}

// Add new property
object.atr_3  = "Hello";
```
Cuando creo el objeto puedo seguir actualizandolo y añadiendo campos
