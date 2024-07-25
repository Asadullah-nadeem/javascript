JavaScript provides several built-in objects that are fundamental to the language and essential for various programming tasks. These objects include constructors for primitive data types, standard objects for working with collections and other data structures, and utility objects for performing common operations. Here’s an overview of some of the most important built-in objects in JavaScript:

### Primitive Wrapper Objects

JavaScript provides wrapper objects for primitive data types to allow them to be used as objects and provide additional functionality:

1. **`String`**
   - Used for creating and manipulating strings.
   ```javascript
   const str = new String("Hello");
   console.log(str.length); // Output: 5
   ```

2. **`Number`**
   - Used for creating and manipulating numbers.
   ```javascript
   const num = new Number(42);
   console.log(num.toFixed(2)); // Output: "42.00"
   ```

3. **`Boolean`**
   - Used for creating and manipulating boolean values.
   ```javascript
   const bool = new Boolean(true);
   console.log(bool.valueOf()); // Output: true
   ```

4. **`Symbol`**
   - Used to create unique and immutable symbols.
   ```javascript
   const sym = Symbol("unique");
   console.log(typeof sym); // Output: "symbol"
   ```

5. **`BigInt`**
   - Used for representing and manipulating large integers.
   ```javascript
   const bigInt = BigInt(9007199254740991);
   console.log(bigInt + 1n); // Output: 9007199254740992n
   ```

### Standard Built-in Objects

1. **`Object`**
   - The base object from which all other objects inherit.
   ```javascript
   const obj = { a: 1, b: 2 };
   console.log(Object.keys(obj)); // Output: ["a", "b"]
   ```

2. **`Array`**
   - Used for creating and manipulating arrays.
   ```javascript
   const arr = [1, 2, 3];
   console.log(arr.length); // Output: 3
   ```

3. **`Function`**
   - Used for creating and manipulating functions.
   ```javascript
   const func = new Function('a', 'b', 'return a + b');
   console.log(func(1, 2)); // Output: 3
   ```

4. **`Date`**
   - Used for working with dates and times.
   ```javascript
   const date = new Date();
   console.log(date.toDateString()); // Output: e.g., "Tue Jul 25 2024"
   ```

5. **`RegExp`**
   - Used for working with regular expressions.
   ```javascript
   const regex = new RegExp("\\d+");
   console.log(regex.test("123")); // Output: true
   ```

6. **`Error`**
   - Used for creating and manipulating error objects.
   ```javascript
   const error = new Error("Something went wrong!");
   console.log(error.message); // Output: "Something went wrong!"
   ```

### Collection Objects

1. **`Map`**
   - Used for creating key-value pairs where keys can be of any type.
   ```javascript
   const map = new Map();
   map.set("key", "value");
   console.log(map.get("key")); // Output: "value"
   ```

2. **`Set`**
   - Used for creating collections of unique values.
   ```javascript
   const set = new Set([1, 2, 3, 3]);
   console.log(set.size); // Output: 3
   ```

3. **`WeakMap`**
   - Similar to `Map`, but keys are weakly referenced.
   ```javascript
   const weakMap = new WeakMap();
   const obj = {};
   weakMap.set(obj, "value");
   console.log(weakMap.get(obj)); // Output: "value"
   ```

4. **`WeakSet`**
   - Similar to `Set`, but values are weakly referenced.
   ```javascript
   const weakSet = new WeakSet();
   const obj = {};
   weakSet.add(obj);
   console.log(weakSet.has(obj)); // Output: true
   ```

### Utility Objects

1. **`Math`**
   - Provides properties and methods for mathematical constants and functions.
   ```javascript
   console.log(Math.PI); // Output: 3.141592653589793
   console.log(Math.sqrt(16)); // Output: 4
   ```

2. **`JSON`**
   - Used for parsing and serializing JSON data.
   ```javascript
   const jsonString = '{"name":"John", "age":30}';
   const obj = JSON.parse(jsonString);
   console.log(obj.name); // Output: "John"
   ```

3. **`Promise`**
   - Represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
   ```javascript
   const promise = new Promise((resolve, reject) => {
     setTimeout(() => resolve("Done!"), 1000);
   });
   promise.then(result => console.log(result)); // Output: "Done!"
   ```

### Summary

JavaScript's built-in objects provide essential functionalities and utilities that are integral to the language. They help in handling various data types, performing operations, managing collections, working with dates, and handling asynchronous operations, among other tasks. Mastering these built-in objects allows developers to write more efficient and effective JavaScript code.
