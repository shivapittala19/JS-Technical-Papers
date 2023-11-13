# Title:  Mutable and Immutable Methods in JavaScript for Strings and Arrays

## 1. Introduction

In JavaScript, data manipulation often involves working with strings and arrays. Mutable methods modify the existing data structures, while immutable methods create new structures, leaving the originals unchanged.

## 2. Mutable Methods in Arrays

Mutable methods directly modify the elements of an array, providing a convenient way to alter data in place.

### 2.1 Example using `splice`:

The `splice` method is a mutable method that allows adding or removing elements from an array.

```javascript
let numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 1, 6); // Removes 1 element at index 2 and adds 6
console.log(numbers); // [1, 2, 6, 4, 5]
```

## 3. Immutable Methods in Arrays

Immutable methods create a new array, leaving the original array unchanged. This approach is beneficial for maintaining data integrity.

### 3.1 Example using `map`:

The `map` method applies a function to each element of an array, returning a new array with the results.

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.map((num) => num * 2);
console.log(doubledNumbers); // [2, 4, 6, 8, 10]
console.log(numbers); // [1, 2, 3, 4, 5] (original array unchanged)
```

## 4. Immutable Methods in Strings

Strings in JavaScript are immutable, meaning that methods return new strings rather than modifying the existing string.

### 4.1 Example using `concat`:

The `concat` method concatenates two strings, creating a new string without altering the original strings.

```javascript
const greeting = 'Hello';
const modifiedGreeting = greeting.concat(', World!');
console.log(modifiedGreeting); // 'Hello, World!'
console.log(greeting); // 'Hello' (original string unchanged)
```
