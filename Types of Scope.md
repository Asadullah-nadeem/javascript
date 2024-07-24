In JavaScript, scope determines the accessibility or visibility of variables and functions. Understanding scope is crucial for writing clean, error-free code. There are several types of scopes in JavaScript:

### Types of Scope

1. **Global Scope**
2. **Local/Function Scope**
3. **Block Scope**
4. **Lexical Scope (Closures)**

### 1. Global Scope

- Variables declared outside any function or block are in the global scope.
- They can be accessed from anywhere in the code.
- In the browser, global variables become properties of the `window` object.

```javascript
var globalVar = "I am global";

function test() {
  console.log(globalVar); // Accessible
}

test();
console.log(globalVar); // Accessible
```

### 2. Local/Function Scope

- Variables declared within a function are in the local scope of that function.
- They are accessible only within that function and not outside.

```javascript
function test() {
  var localVar = "I am local";
  console.log(localVar); // Accessible
}

test();
console.log(localVar); // Uncaught ReferenceError: localVar is not defined
```

### 3. Block Scope

- Variables declared with `let` or `const` within a block `{}` are block-scoped.
- They are accessible only within that block.

```javascript
if (true) {
  let blockVar = "I am block scoped";
  console.log(blockVar); // Accessible
}

console.log(blockVar); // Uncaught ReferenceError: blockVar is not defined
```

- `var` does not create block scope but function scope.

```javascript
if (true) {
  var functionScopedVar = "I am function scoped";
}

console.log(functionScopedVar); // Accessible
```

### 4. Lexical Scope (Closures)

- Lexical scope refers to the scope determined by the physical placement of the code.
- Inner functions have access to variables of their outer functions due to closures.

```javascript
function outer() {
  var outerVar = "I am outer";

  function inner() {
    console.log(outerVar); // Accessible due to closure
  }

  inner();
}

outer();
```

### Scope Chain

- When trying to access a variable, JavaScript starts looking in the current scope and moves up the scope chain to the outer scopes until it finds the variable or reaches the global scope.
- If the variable is not found, a `ReferenceError` is thrown.

```javascript
var globalVar = "I am global";

function outer() {
  var outerVar = "I am outer";

  function inner() {
    var innerVar = "I am inner";
    console.log(innerVar);  // Accessible
    console.log(outerVar);  // Accessible due to closure
    console.log(globalVar); // Accessible
  }

  inner();
}

outer();
```

### Variable Shadowing

- A variable declared in an inner scope can shadow a variable with the same name in an outer scope.

```javascript
var shadowVar = "I am global";

function test() {
  var shadowVar = "I am local";
  console.log(shadowVar); // "I am local"
}

test();
console.log(shadowVar); // "I am global"
```

### Hoisting and Scope

- Variable and function declarations are hoisted to the top of their scope.
- `let` and `const` declarations are hoisted but not initialized, resulting in a `ReferenceError` if accessed before declaration.

```javascript
console.log(hoistedVar); // undefined (due to hoisting)
var hoistedVar = "I am hoisted";

function hoistedFunction() {
  console.log("I am hoisted function");
}
hoistedFunction(); // Accessible

console.log(letVar); // ReferenceError: Cannot access 'letVar' before initialization
let letVar = "I am let variable";
```
