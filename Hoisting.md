### Hoisting in JavaScript

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during the compile phase, before the code executes. This means that you can use variables and functions before they are actually declared in the code.

For example:

```javascript
console.log(myVar); // Output: undefined
var myVar = 5;
```

In the code above, `myVar` is hoisted to the top of its scope, so the declaration happens before the console log, but the assignment of `5` happens later, which is why the output is `undefined`.

### Interview Questions on Hoisting (without solutions)

1. What is hoisting in JavaScript and how does it affect the way you write code?
2. How does hoisting differ between variable declarations with `var`, `let`, and `const`?
3. Can you explain how function declarations and function expressions are affected by hoisting?
4. How does JavaScript handle the hoisting of variables and functions within the same scope?
5. What are some common issues or bugs that can occur due to hoisting in JavaScript?

### Interview Questions on Hoisting (with solutions)

1. **What is hoisting in JavaScript and how does it affect the way you write code?**

   **Answer:**
   Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compile phase, before the code executes. This means you can use variables and functions before they are actually declared in the code. Understanding hoisting helps avoid errors and write clearer code by being aware of how declarations are handled.

   ```javascript
   console.log(myVar); // Output: undefined
   var myVar = 5;
   ```
   In the example above, `myVar` is hoisted to the top, so the declaration happens before the console log, resulting in `undefined`.

2. **How does hoisting differ between variable declarations with `var`, `let`, and `const`?**

   **Answer:**
   - **`var`**: Variables declared with `var` are hoisted to the top of their scope and initialized with `undefined`. This can lead to unexpected behavior if not used carefully.

     ```javascript
     console.log(varVar); // Output: undefined
     var varVar = 10;
     ```

   - **`let` and `const`**: Variables declared with `let` and `const` are hoisted but not initialized. Accessing them before declaration results in a `ReferenceError` due to the temporal dead zone (TDZ).

     ```javascript
     console.log(letVar); // ReferenceError: Cannot access 'letVar' before initialization
     let letVar = 10;

     console.log(constVar); // ReferenceError: Cannot access 'constVar' before initialization
     const constVar = 10;
     ```

3. **Can you explain how function declarations and function expressions are affected by hoisting?**

   **Answer:**
   - **Function Declarations**: Entire function declarations are hoisted, allowing them to be called before their definition in the code.

     ```javascript
     hoistedFunction(); // Output: "Hello, World!"

     function hoistedFunction() {
       console.log("Hello, World!");
     }
     ```

   - **Function Expressions**: Only the variable declaration is hoisted, not the assignment. Therefore, calling a function expression before its definition results in an error.

     ```javascript
     console.log(hoistedExpression); // Output: undefined
     hoistedExpression(); // TypeError: hoistedExpression is not a function

     var hoistedExpression = function() {
       console.log("Hello, World!");
     };
     ```

4. **How does JavaScript handle the hoisting of variables and functions within the same scope?**

   **Answer:**
   JavaScript hoists both variable and function declarations to the top of their scope. Function declarations take precedence over variable declarations, but variable assignments do not overwrite functions.

   ```javascript
   console.log(hoisted); // Output: [Function: hoisted]

   var hoisted = 10;

   function hoisted() {
     console.log("Function");
   }

   console.log(hoisted); // Output: 10
   ```
   In the example above, the function declaration `hoisted` is hoisted first, but later the variable assignment `hoisted = 10` overrides the function.

5. **What are some common issues or bugs that can occur due to hoisting in JavaScript?**

   **Answer:**
   - **Unexpected `undefined` Values**: Accessing variables declared with `var` before their assignment can lead to `undefined` values.

     ```javascript
     console.log(myVar); // Output: undefined
     var myVar = 5;
     ```

   - **ReferenceError with `let` and `const`**: Accessing variables declared with `let` or `const` before their declaration results in a `ReferenceError`.

     ```javascript
     console.log(letVar); // ReferenceError
     let letVar = 5;
     ```

   - **Function and Variable Name Conflicts**: Declaring a variable with the same name as a function can lead to unexpected behavior.

     ```javascript
     var func;
     function func() {
       console.log("Function");
     }
     console.log(func); // Output: undefined
     ```

