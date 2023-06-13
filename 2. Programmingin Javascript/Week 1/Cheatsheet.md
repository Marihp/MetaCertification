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
