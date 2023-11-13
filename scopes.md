# Title: Navigating Scopes in JavaScript

## 1. Introduction

Scopes in JavaScript define the context in which variables and functions are accessible. Understanding the intricacies of lexical scope, function scope, and block scope is essential for writing maintainable and bug-free code.

## 2. Lexical Scope

### 2.1 Definition

Lexical scope, also known as static scope, is determined at the time of code writing. It is based on the physical placement of functions and blocks in the code.

### 2.2 Example

```javascript
function outer() {
  let outerVar = 'I am from outer';

  function inner() {
    console.log(outerVar); // Accessible due to lexical scope
  }

  inner();
}

outer(); // Output: 'I am from outer'
```

## 3. Function Scope

### 3.1 Definition

Function scope means that variables declared inside a function are accessible only within that function.

### 3.2 Example

```javascript
function example() {
  if (true) {
    var insideIf = 'I am inside if'; // Function scope
  }
  console.log(insideIf); // Output: 'I am inside if'
}

example();
```

## 4. Block Scope

### 4.1 Definition

Block scope, introduced with `let` and `const`, confines variables to the block in which they are defined.

### 4.2 Example

```javascript
function example() {
  if (true) {
    let insideIf = 'I am inside if'; // Block scope
  }
  console.log(insideIf); // ReferenceError: insideIf is not defined
}

example();
```