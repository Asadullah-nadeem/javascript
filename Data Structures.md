In JavaScript, data structures are essential for organizing, storing, and managing data efficiently. Here’s an overview of the key data structures available in JavaScript:

### 1. Arrays

**Description**: Arrays are ordered collections of elements. They can hold values of any type and support various operations for manipulation and access.

**Creating Arrays**:
```javascript
const fruits = ["Apple", "Banana", "Cherry"];
```

**Common Operations**:
- **Accessing Elements**: `fruits[0]` // "Apple"
- **Adding Elements**:
  - At the end: `fruits.push("Date")`
  - At the beginning: `fruits.unshift("Apricot")`
- **Removing Elements**:
  - From the end: `fruits.pop()`
  - From the beginning: `fruits.shift()`
- **Finding Elements**: `fruits.indexOf("Banana")` // 1
- **Iterating**: `fruits.forEach(fruit => console.log(fruit))`

### 2. Objects

**Description**: Objects are collections of key-value pairs where keys are strings (or Symbols) and values can be any type. They are useful for representing entities with properties and methods.

**Creating Objects**:
```javascript
const person = {
  name: "John",
  age: 30,
  greet() {
    console.log("Hello, " + this.name);
  }
};
```

**Common Operations**:
- **Accessing Values**: `person.name` // "John"
- **Adding Properties**: `person.email = "john@example.com"`
- **Deleting Properties**: `delete person.age`
- **Iterating**: `Object.keys(person).forEach(key => console.log(key, person[key]))`

### 3. Sets

**Description**: A Set is a collection of unique values. Sets are useful for storing values without duplicates.

**Creating Sets**:
```javascript
const numbers = new Set([1, 2, 3, 4]);
```

**Common Operations**:
- **Adding Values**: `numbers.add(5)`
- **Deleting Values**: `numbers.delete(2)`
- **Checking Presence**: `numbers.has(3)` // true
- **Iterating**: `numbers.forEach(num => console.log(num))`

### 4. Maps

**Description**: A Map is a collection of key-value pairs where keys can be of any type. Maps maintain the insertion order of keys.

**Creating Maps**:
```javascript
const map = new Map();
map.set('name', 'John');
map.set('age', 30);
```

**Common Operations**:
- **Adding Key-Value Pairs**: `map.set('email', 'john@example.com')`
- **Accessing Values**: `map.get('name')` // "John"
- **Deleting Key-Value Pairs**: `map.delete('age')`
- **Checking Presence**: `map.has('name')` // true
- **Iterating**: `map.forEach((value, key) => console.log(key, value))`

### 5. WeakSets

**Description**: A WeakSet is a collection of objects where the references to objects are weak. This means that objects in a WeakSet can be garbage-collected if they are no longer in use elsewhere.

**Creating WeakSets**:
```javascript
const weakSet = new WeakSet();
const obj = {};
weakSet.add(obj);
```

**Common Operations**:
- **Adding Objects**: `weakSet.add(obj)`
- **Deleting Objects**: `weakSet.delete(obj)`
- **Checking Presence**: `weakSet.has(obj)` // true

### 6. WeakMaps

**Description**: A WeakMap is a collection of key-value pairs where keys are objects and the references to the keys are weak. This allows objects to be garbage-collected if they are not referenced elsewhere.

**Creating WeakMaps**:
```javascript
const weakMap = new WeakMap();
const obj = {};
weakMap.set(obj, "value");
```

**Common Operations**:
- **Adding Key-Value Pairs**: `weakMap.set(obj, 'value')`
- **Accessing Values**: `weakMap.get(obj)` // "value"
- **Deleting Key-Value Pairs**: `weakMap.delete(obj)`
- **Checking Presence**: `weakMap.has(obj)` // true

### 7. Typed Arrays

**Description**: Typed Arrays provide a way to work with binary data in an array-like format. They are useful for handling raw binary data, such as when interacting with Web APIs.

**Common Types**:
- `Int8Array`
- `Uint8Array`
- `Uint16Array`
- `Float32Array`

**Creating Typed Arrays**:
```javascript
const intArray = new Int32Array([1, 2, 3, 4]);
```

**Common Operations**:
- **Accessing Elements**: `intArray[0]` // 1
- **Setting Elements**: `intArray[1] = 5`
- **Iterating**: `intArray.forEach(value => console.log(value))`

### Summary

JavaScript provides a variety of data structures to efficiently manage and manipulate data. Choosing the right data structure depends on the specific needs of your application, such as whether you need ordered collections, unique values, or key-value pairs. Understanding these data structures and their operations is crucial for writing effective and efficient JavaScript code.
