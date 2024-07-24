In JavaScript, there are specific rules and conventions for naming variables, functions, and other identifiers. Following these rules ensures that your code is syntactically correct and more readable. Here are the key naming rules and conventions:

### Naming Rules

1. **Start with a Letter, Underscore, or Dollar Sign**:
   - Identifiers must begin with a letter (a-z, A-Z), an underscore (_), or a dollar sign ($).
   - Example: `myVariable`, `_privateVar`, `$price`

2. **Followed by Letters, Digits, Underscores, or Dollar Signs**:
   - Subsequent characters can include letters, digits (0-9), underscores, or dollar signs.
   - Example: `var2`, `total_amount`, `price$`

3. **Case Sensitivity**:
   - Identifiers are case-sensitive. `myVar` and `myvar` are considered different.
   - Example: `MyVar` and `myVar` are two distinct variables.

4. **Reserved Keywords**:
   - Reserved keywords in JavaScript cannot be used as identifiers.
   - Example: `var`, `function`, `return`, `class`, `if`, `else`, etc.
   - Incorrect: `var var = 10;` (invalid because `var` is a keyword)

### Naming Conventions

1. **Camel Case for Variables and Functions**:
   - Use camelCase for naming variables and functions. The first word is lowercase, and subsequent words start with a capital letter.
   - Example: `myVariable`, `calculateTotal`, `fetchData`

2. **Pascal Case for Classes and Constructors**:
   - Use PascalCase for naming classes and constructor functions. Each word starts with a capital letter.
   - Example: `Person`, `Car`, `DataManager`

3. **Constants in Uppercase**:
   - Use uppercase letters separated by underscores for naming constants.
   - Example: `MAX_HEIGHT`, `DEFAULT_COLOR`, `PI`

4. **Descriptive Names**:
   - Use meaningful and descriptive names that indicate the purpose of the variable or function.
   - Example: `calculateArea` (instead of `calcA`), `userAge` (instead of `ua`)

5. **Avoid Single-Letter Names**:
   - Avoid using single-letter names except for loop counters or very short functions.
   - Example: `index`, `counter` (instead of `i`, `c`)

6. **Avoid Leading Underscores for Public Variables**:
   - Leading underscores are typically used to indicate private variables in some coding conventions.
   - Example: `_privateVar` (used internally)

### Examples

```javascript
// Valid variable names
var myVariable;
var _privateVar;
var $price;
var totalAmount2;

// Valid function names
function calculateTotal() {
  // Function body
}

function _privateFunction() {
  // Function body
}

// Valid class name
class DataManager {
  // Class body
}

// Valid constant
const MAX_HEIGHT = 500;

// Invalid names (will cause syntax errors)
var 2variable;        // Cannot start with a digit
var my-var;           // Cannot contain hyphens
var function;         // Cannot use reserved keywords
```
