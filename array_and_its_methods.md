# js array and its magic fuctions


JavaScript arrays are one of the fundamental data structures in the language, allowing you to store and manipulate collections of elements. Arrays in JavaScript can hold various types of data, including numbers, strings, objects, and even other arrays. Here’s a breakdown of some basic array concepts and some "magic" functions commonly used with arrays:

### Array Basics

1. **Creating Arrays:**
   ```javascript
   let fruits = ['Apple', 'Banana', 'Cherry'];
   let numbers = [1, 2, 3, 4, 5];
   ```

2. **Accessing Elements:**
   You can access elements using their index, starting from 0.
   ```javascript
   console.log(fruits[0]); // Output: 'Apple'
   ```

3. **Modifying Elements:**
   You can modify elements directly by assigning a new value to the desired index.
   ```javascript
   fruits[1] = 'Orange';
   ```

4. **Array Length:**
   You can get the number of elements in an array using the `length` property.
   ```javascript
   console.log(fruits.length); // Output: 3
   ```

### Magic Functions (Array Methods)

JavaScript arrays come with many built-in methods that make working with arrays easier and more efficient. Here are some commonly used "magic" functions:

1. **`push()` and `pop()`:**
   - `push()`: Adds one or more elements to the end of an array.
   - `pop()`: Removes the last element from an array and returns it.

   ```javascript
   fruits.push('Grapes'); // ['Apple', 'Orange', 'Cherry', 'Grapes']
   let lastFruit = fruits.pop(); // 'Grapes'; fruits: ['Apple', 'Orange', 'Cherry']
   ```


2. **`unshift()` and `shift()`:**
   - `unshift()`: Adds one or more elements to the beginning of an array.
   - `shift()`: Removes the first element from an array and returns it.

  
   ```javascript
   fruits.unshift('Mango'); // ['Mango', 'Apple', 'Orange', 'Cherry']
   let firstFruit = fruits.shift(); // 'Mango'; fruits: ['Apple', 'Orange', 'Cherry']
   ```

3. **`splice()`:**
   Allows you to add/remove elements from anywhere in an array.
   ```javascript
   fruits.splice(1, 0, 'Pear'); // ['Apple', 'Pear', 'Orange', 'Cherry']
   fruits.splice(2, 1); // ['Apple', 'Pear', 'Cherry']
   ```

4. **`slice()`:**
   Returns a shallow copy of a portion of an array into a new array.
   ```javascript
   let slicedFruits = fruits.slice(1, 3); // ['Pear', 'Cherry']; original array is unchanged
   ```

5. **`concat()`:**
   Combines two or more arrays into a new array.
   ```javascript
   let moreFruits = ['Grapes', 'Pineapple'];
   let allFruits = fruits.concat(moreFruits); // ['Apple', 'Pear', 'Cherry', 'Grapes', 'Pineapple']
   ```

6. **`forEach()`:**
   Executes a provided function once for each array element.
   ```javascript
   fruits.forEach(function(fruit) {
       console.log(fruit);
   });
   ```

7. **`map()`:**
   Creates a new array populated with the results of calling a provided function on every element in the calling array.
   ```javascript
   let fruitLengths = fruits.map(function(fruit) {
       return fruit.length;
   });
   ```

8. **`filter()`:**
   Creates a new array with all elements that pass the test implemented by the provided function.
   ```javascript
   let shortFruits = fruits.filter(function(fruit) {
       return fruit.length < 6;
   });
   ```

These are just a few examples of what you can do with JavaScript arrays. There are many other array methods available, each serving different purposes and making array manipulation more convenient and expressive.

---
# Details about **forEach, map, filter**:

Let's dive deeper into `forEach`, `map`, and `filter` array methods in JavaScript with examples and proper outputs.

### `forEach()`

The `forEach()` method executes a provided function once for each array element.

**Syntax:**
```javascript
array.forEach(function(currentValue, index, array) {
    // Your code here
});
```

**Example:**
```javascript
let numbers = [1, 2, 3, 4, 5];

numbers.forEach(function(number, index) {
    console.log(`Number at index ${index}: ${number}`);
});
```

**Output:**
```
Number at index 0: 1
Number at index 1: 2
Number at index 2: 3
Number at index 3: 4
Number at index 4: 5
```

In this example, `forEach` iterates over each element of the `numbers` array and logs each number along with its index to the console.

### `map()`

The `map()` method creates a new array with the results of calling a provided function on every element in the calling array.

**Syntax:**
```javascript
let newArray = array.map(function(currentValue, index, array) {
    return // transformation or computation
});
```

**Example:**
```javascript
let numbers = [1, 2, 3, 4, 5];

let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});

console.log(doubledNumbers);
```

**Output:**
```
[2, 4, 6, 8, 10]
```

Here, `map()` applies the function (multiplying each number by 2) to every element in the `numbers` array, creating a new array `doubledNumbers` with the transformed values.

### `filter()`

The `filter()` method creates a new array with all elements that pass the test implemented by the provided function.

**Syntax:**
```javascript
let newArray = array.filter(function(currentValue, index, array) {
    return // true or false based on some condition
});
```

**Example:**
```javascript
let numbers = [1, 2, 3, 4, 5];

let evenNumbers = numbers.filter(function(number) {
    return number % 2 === 0;
});

console.log(evenNumbers);
```

**Output:**
```
[2, 4]
```

In this example, `filter()` creates a new array `evenNumbers` containing only the elements from `numbers` that are even (passing the condition `number % 2 === 0`).

These methods (`forEach`, `map`, `filter`) are powerful and commonly used for array manipulation in JavaScript. They provide a concise and expressive way to perform operations on arrays without needing to write explicit loops or conditions.


