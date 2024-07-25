Primitive types in JavaScript are the most basic data types and are not objects. These types are immutable, meaning their values cannot be changed. When you work with a primitive type, you are directly dealing with the value itself rather than a reference to an object. JavaScript has seven primitive data types:

### 1. Undefined

- **Type**: `undefined`
- **Description**: Represents a variable that has been declared but not assigned a value.
  
```javascript
let x;
console.log(x); // Output: undefined
console.log(typeof x); // Output: "undefined"
```

### 2. Null

- **Type**: `object` (This is a quirk in JavaScript; `null` is considered a primitive type but `typeof null` returns "object".)
- **Description**: Represents the intentional absence of any object value.

```javascript
let y = null;
console.log(y); // Output: null
console.log(typeof y); // Output: "object"
```

### 3. Boolean

- **Type**: `boolean`
- **Description**: Represents a logical entity and can have two values: `true` or `false`.

```javascript
let isTrue = true;
let isFalse = false;
console.log(typeof isTrue); // Output: "boolean"
console.log(typeof isFalse); // Output: "boolean"
```

### 4. Number

- **Type**: `number`
- **Description**: Represents both integer and floating-point numbers.

```javascript
let num = 42;
let float = 3.14;
console.log(typeof num); // Output: "number"
console.log(typeof float); // Output: "number"
```

- **Special Values**:
  - `Infinity`
  - `-Infinity`
  - `NaN` (Not-a-Number)

```javascript
console.log(typeof Infinity); // Output: "number"
console.log(typeof NaN); // Output: "number"
console.log(0 / 0); // Output: NaN
```

### 5. String

- **Type**: `string`
- **Description**: Represents a sequence of characters.

```javascript
let str = "Hello, World!";
console.log(typeof str); // Output: "string"
```

### 6. Symbol

- **Type**: `symbol`
- **Description**: Represents a unique and immutable value, often used as an identifier for object properties.

```javascript
let sym = Symbol("description");
console.log(typeof sym); // Output: "symbol"
```

### 7. BigInt

- **Type**: `bigint`
- **Description**: Represents whole numbers larger than `2^53 - 1` (the largest number JavaScript can reliably represent with the `number` type).

```javascript
let bigInt = BigInt(9007199254740991);
console.log(typeof bigInt); // Output: "bigint"
```

### Differences Between Primitives and Objects

1. **Immutability**: Primitive values are immutable. When you assign a primitive value to a variable, any operations on that variable create a new value.
  
```javascript
let str1 = "Hello";
let str2 = str1;
str2 = "World";
console.log(str1); // Output: "Hello"
console.log(str2); // Output: "World"
```

2. **Reference**: Objects are mutable and are accessed by reference. When you assign an object to a variable, the variable holds a reference to the object, not the object itself.
  
```javascript
let obj1 = { a: 1 };
let obj2 = obj1;
obj2.a = 2;
console.log(obj1.a); // Output: 2
console.log(obj2.a); // Output: 2
```

### Wrapper Objects

JavaScript provides wrapper objects for primitive types (except `null` and `undefined`) so that you can use them like objects and call methods on them.

```javascript
let str = "Hello, World!";
console.log(str.length); // Output: 13
console.log(str.toUpperCase()); // Output: "HELLO, WORLD!"
```

### Type Conversion

JavaScript automatically converts between primitives and their corresponding wrapper objects when necessary.

```javascript
let num = 42;
let str = num.toString(); // num is temporarily converted to Number object
console.log(typeof str); // Output: "string"
```

### Summary

Primitive types are the most basic data types in JavaScript. They are immutable and are directly manipulated as values. Understanding these types and their behaviors is fundamental to working with JavaScript effectively.
