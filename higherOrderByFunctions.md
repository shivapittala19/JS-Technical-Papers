# Title: Higher-Order Functions in JavaScript

## 1. Introduction

Higher-order functions are a key feature of functional programming in JavaScript. Understanding higher-order functions is essential for writing code that is both efficient and expressive.

## 2. Definition

### 2.1 What are Higher-Order Functions?

A higher-order function is a function that either takes one or more functions as arguments or returns a function as its result.

## 3. Working with Higher-Order Functions

### 3.1 Functions as Parameters

Higher-order functions can accept other functions as parameters, enabling the creation of more flexible and reusable code.

```javascript
function operateOnNumbers(a, b, operation) {
  return operation(a, b);
}

function add(x, y) {
  return x + y;
}

function multiply(x, y) {
  return x * y;
}

console.log(operateOnNumbers(3, 4, add)); // Output: 7
console.log(operateOnNumbers(3, 4, multiply)); // Output: 12
```


## 4. Practical Applications

### 4.1 Map, Filter, and Reduce

Higher-order functions like `map`, `filter`, and `reduce` provide concise ways to manipulate arrays.

```javascript
let numbers = [1, 2, 3, 4, 5];

// Using map to double each element
let doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8, 10]

// Using filter to get even numbers
let evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // Output: [2, 4]

// Using reduce to calculate the sum
let sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // Output: 15
```


## 5. Benefits of Higher-Order Functions

### 5.1 Code Reusability

Higher-order functions promote code reusability by encapsulating generic operations that can be applied to various contexts.

### 5.2 Readability

Using higher-order functions often results in more readable and declarative code, reducing the need for explicit loops and conditional statements.

