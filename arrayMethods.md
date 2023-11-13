# Title: A Comprehensive Guide to Array Methods in JavaScript

## 1. Basics

### 1.1 Array.pop (Mutable)

Removes the last element from an array and returns that element.

```javascript
let fruits = ['apple', 'banana', 'orange'];
let removed = fruits.pop();
console.log(removed); // Output: 'orange'
console.log(fruits); // Output: ['apple', 'banana']
```

### 1.2 Array.push (Mutable)

Adds one or more elements to the end of an array and returns the new length.

```javascript
let fruits = ['apple', 'banana'];
let newLength = fruits.push('orange');
console.log(newLength); // Output: 3
console.log(fruits); // Output: ['apple', 'banana', 'orange']
```

### 1.3 Array.concat (Immutable)

Merges two or more arrays, creating a new array without modifying the original arrays.

```javascript
let fruits1 = ['apple', 'banana'];
let fruits2 = ['orange', 'grape'];
let mergedFruits = fruits1.concat(fruits2);
console.log(mergedFruits); // Output: ['apple', 'banana', 'orange', 'grape']
console.log(fruits1); // Output: ['apple', 'banana'] (unchanged)
```

### 1.4 Array.slice (Immutable)

Returns a shallow copy of a portion of an array into a new array.

```javascript
let fruits = ['apple', 'banana', 'orange', 'grape'];
let slicedFruits = fruits.slice(1, 3);
console.log(slicedFruits); // Output: ['banana', 'orange']
console.log(fruits); // Output: ['apple', 'banana', 'orange', 'grape'] (unchanged)
```

### 1.5 Array.splice (Mutable)

Changes the contents of an array by removing or replacing elements.

```javascript
let fruits = ['apple', 'banana', 'orange', 'grape'];
fruits.splice(2, 1, 'kiwi');
console.log(fruits); // Output: ['apple', 'banana', 'kiwi', 'grape']
```

### 1.6 Array.join (Immutable)

Creates and returns a new string by concatenating all the elements in an array.

```javascript
let fruits = ['apple', 'banana', 'orange'];
let joinedString = fruits.join(', ');
console.log(joinedString); // Output: 'apple, banana, orange'
console.log(fruits); // Output: ['apple', 'banana', 'orange'] (unchanged)
```

### 1.7 Array.flat (Immutable)

Creates a new array with all sub-array elements concatenated recursively.

```javascript
let nestedArray = [1, 2, [3, 4, [5, 6]]];
let flatArray = nestedArray.flat(2);
console.log(flatArray); // Output: [1, 2, 3, 4, 5, 6]
console.log(nestedArray); // Output: [1, 2, [3, 4, [5, 6]]] (unchanged)
```

## 2. Finding

### 2.1 Array.find (Immutable)

Returns the first element in an array that satisfies a provided testing function.

```javascript
let numbers = [10, 20, 30, 40];
let found = numbers.find(num => num > 25);
console.log(found); // Output: 30
console.log(numbers); // Output: [10, 20, 30, 40] (unchanged)
```

### 2.2 Array.indexOf (Immutable)

Returns the first index at which a given element can be found in the array, or -1 if it is not present.

```javascript
let fruits = ['apple', 'banana', 'orange'];
let index = fruits.indexOf('banana');
console.log(index); // Output: 1
console.log(fruits); // Output: ['apple', 'banana', 'orange'] (unchanged)
```

### 2.3 Array.includes (Immutable)

Checks if an array includes a certain element, returning true or false.

```javascript
let fruits = ['apple', 'banana', 'orange'];
let includesOrange = fruits.includes('orange');
console.log(includesOrange); // Output: true
console.log(fruits); // Output: ['apple', 'banana', 'orange'] (unchanged)
```

### 2.4 Array.findIndex (Immutable)

Returns the index of the first element in an array that satisfies a provided testing function.

```javascript
let numbers = [10, 20, 30, 40];
let index = numbers.findIndex(num => num > 25);
console.log(index); // Output: 2
console.log(numbers); // Output: [10, 20, 30, 40] (unchanged)
```

## 3. Higher Order Functions

### 3.1 Array.forEach (Mutable)

Executes a provided function once for each array element.

```javascript
let numbers = [1, 2, 3];
numbers.forEach(num => console.log(num * 2));
// Output:
// 2
// 4
// 6
console.log(numbers); // Output: [1, 2, 3] (unchanged)
```

### 3.2 Array.filter (Immutable)

Creates a new array with all elements that pass the test implemented by the provided function.

```javascript
let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
console.log(numbers); // Output: [1, 2, 3, 4, 5] (unchanged)
```

### 3.3 Array.map (Immutable)

Creates a new array with the results of calling a provided function on every element in the array.

```javascript
let numbers = [1, 2, 3];
let squaredNumbers = numbers.map(num => num ** 2);
console.log(squaredNumbers); // Output: [1, 4, 9]
console.log(numbers); // Output: [1, 2, 3] (unchanged)
```

### 3.4 Array.reduce (Immutable)

Applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // Output: 10
console.log(numbers); // Output: [1, 2, 3, 4] (unchanged)
```

### 3.5 Array.sort (Mutable)

Sorts the elements of an array in place.

```javascript
let fruits = ['banana', 'apple', 'orange'];
fruits.sort();
console.log(fruits); // Output: ['