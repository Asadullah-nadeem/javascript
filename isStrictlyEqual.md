The `isStrictlyEqual` function checks whether two values are strictly equal, meaning both the value and the type must be the same. This is the same behavior as JavaScript’s strict equality operator (`===`).

Here’s how you can implement the `isStrictlyEqual` function in JavaScript:

### Implementation of `isStrictlyEqual`

```javascript
function isStrictlyEqual(value1, value2) {
  return value1 === value2;
}

// Examples
console.log(isStrictlyEqual(5, 5));           // Output: true
console.log(isStrictlyEqual(5, '5'));         // Output: false (different types)
console.log(isStrictlyEqual('hello', 'hello')); // Output: true
console.log(isStrictlyEqual(null, undefined)); // Output: false (different types)
console.log(isStrictlyEqual([], []));          // Output: false (different object references)
console.log(isStrictlyEqual([1, 2], [1, 2]));  // Output: false (different object references)
console.log(isStrictlyEqual(NaN, NaN));        // Output: false (NaN is not equal to NaN)
```

### Explanation

- **Direct Comparison**: The function uses the strict equality operator (`===`) to compare `value1` and `value2`. This operator checks both the type and the value, ensuring that they are identical.

### Key Points About Strict Equality

1. **Type Matching**: The values must be of the same type. For example, the number `5` and the string `'5'` are not strictly equal because they are different types.

2. **Object Comparisons**: For objects (including arrays), strict equality checks whether they refer to the same instance. Two distinct objects with the same content are not considered strictly equal because they are different references.

3. **NaN Special Case**: In JavaScript, `NaN` is not equal to itself, so `NaN === NaN` returns `false`. This is a known peculiarity in JavaScript.

By using `isStrictlyEqual`, you ensure that both the type and value of the two compared entities are exactly the same, which is essential for precise comparisons in JavaScript.
