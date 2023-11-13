# Title: Understanding Pass by Reference and Pass by Value in JavaScript

## 1. Introduction

JavaScript employs both pass by reference and pass by value mechanisms when dealing with data. 

## 2. Pass by Value

In pass by value, a copy of the data is passed to a function, leaving the original data unchanged. This is common for primitive data types.

### 2.1 Example with Numbers (Primitive Type):

```javascript
function modifyNumber(num) {
  num = 10; // Changes local copy, not the original
}

let originalNumber = 5;
modifyNumber(originalNumber);
console.log(originalNumber); // Output: 5 (unchanged)
```

### 2.2 Example with Strings (Primitive Type):

```javascript
function modifyString(str) {
  str = 'Modified'; // Changes local copy, not the original
}

let originalString = 'Original';
modifyString(originalString);
console.log(originalString); // Output: 'Original' (unchanged)
```

## 3. Pass by Reference

In pass by reference, a reference to the original data is passed to a function. Changes made to the data within the function affect the original data.

### 3.1 Example with Arrays (Reference Type):

```javascript
function modifyArray(arr) {
  arr.push(4); // Modifies the original array
}

let originalArray = [1, 2, 3];
modifyArray(originalArray);
console.log(originalArray); // Output: [1, 2, 3, 4] (modified)
```

### 3.2 Example with Objects (Reference Type):

```javascript
function modifyObject(obj) {
  obj.property = 'Modified'; // Modifies the original object
}

let originalObject = { property: 'Original' };
modifyObject(originalObject);
console.log(originalObject.property); // Output: 'Modified' (modified)
```
