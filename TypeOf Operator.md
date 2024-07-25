The `typeof` operator in JavaScript is used to determine the type of a given value. It returns a string indicating the type of the unevaluated operand. Understanding how `typeof` works is essential for type checking and debugging in JavaScript.

### Syntax

```javascript
typeof operand
```

### Common Use Cases

Here are some common types and what `typeof` returns for each:

1. **Primitive Types**:
   - `typeof undefined` returns `"undefined"`
   - `typeof true` returns `"boolean"`
   - `typeof 42` returns `"number"`
   - `typeof "Hello"` returns `"string"`
   - `typeof Symbol("symbol")` returns `"symbol"`
   - `typeof BigInt(10)` returns `"bigint"`

2. **Special Case**:
   - `typeof null` returns `"object"` (This is a well-known JavaScript quirk. `null` is a primitive value, but `typeof` returns `"object"`.)

3. **Function**:
   - `typeof function() {}` returns `"function"`

4. **Object**:
   - `typeof {}` returns `"object"`
   - `typeof []` returns `"object"` (Arrays are a type of object)

### Examples

#### Basic Usage

```javascript
console.log(typeof undefined); // "undefined"
console.log(typeof true);      // "boolean"
console.log(typeof 42);        // "number"
console.log(typeof "Hello");   // "string"
console.log(typeof Symbol("symbol")); // "symbol"
console.log(typeof BigInt(10)); // "bigint"
console.log(typeof null);      // "object" (a quirk of JavaScript)
console.log(typeof function(){}); // "function"
console.log(typeof {});        // "object"
console.log(typeof []);        // "object"
```

#### Type Checking in Conditional Statements

```javascript
const value = "Hello";

if (typeof value === "string") {
  console.log("The value is a string.");
} else {
  console.log("The value is not a string.");
}

// Output: "The value is a string."
```

#### Handling Different Types

```javascript
function processInput(input) {
  if (typeof input === "string") {
    console.log("Processing a string: " + input);
  } else if (typeof input === "number") {
    console.log("Processing a number: " + input);
  } else if (typeof input === "object" && input !== null) {
    console.log("Processing an object");
  } else {
    console.log("Unknown type: " + typeof input);
  }
}

processInput("Hello"); // "Processing a string: Hello"
processInput(42); // "Processing a number: 42"
processInput({}); // "Processing an object"
processInput(null); // "Unknown type: object"
```

### Special Cases and Caveats

- **Arrays**:
  - Although `typeof []` returns `"object"`, you can use `Array.isArray()` to check if an object is an array.

```javascript
const arr = [1, 2, 3];
console.log(typeof arr); // "object"
console.log(Array.isArray(arr)); // true
```

- **null**:
  - As mentioned, `typeof null` returns `"object"`. To check for `null`, use strict equality `===`.

```javascript
const value = null;
console.log(typeof value); // "object"
console.log(value === null); // true
```

- **Functions**:
  - The `typeof` operator returns `"function"` for functions, making it easy to distinguish them from other objects.

```javascript
function myFunction() {}
console.log(typeof myFunction); // "function"
```

### Summary

The `typeof` operator is a simple yet powerful tool for type checking in JavaScript. It helps you determine the type of a variable or expression, allowing you to write more robust and error-resistant code. However, be aware of its quirks, such as the behavior with `null` and arrays, to use it effectively.
