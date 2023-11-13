# Title:  Hoisting in JavaScript

## 1. Introduction

Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase. While this might seem counterintuitive, understanding hoisting is crucial for writing reliable and maintainable code.

## 2. Variable Hoisting

### 2.1 Variable Declaration

Variable declarations are hoisted to the top of their scope but not their assignments.

```javascript
console.log(x); // Output: undefined
var x = 5;
console.log(x); // Output: 5
```

### 2.2 let and const Declarations

Unlike `var`, `let` and `const` declarations are hoisted but not initialized. Accessing them before the declaration results in a `ReferenceError`.

```javascript
console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;
console.log(y); // Output: 10
```

## 3. Function Hoisting

### 3.1 Function Declaration

Function declarations are fully hoisted, allowing them to be called before the declaration.

```javascript
greet(); // Output: 'Hello, World!'
function greet() {
  console.log('Hello, World!');
}
```

### 3.2 Function Expression

Function expressions are hoisted differently. Only the variable declaration is hoisted, not the function assignment.

```javascript
sayHello(); // TypeError: sayHello is not a function
var sayHello = function() {
  console.log('Hello!');
};
```

## 4. Hoisting Best Practices

### 4.1 Declare Variables at the Top

To avoid unexpected behavior, it's best to declare variables at the top of their scope.

```javascript
function example() {
  var a;
  if (condition) {
    var b;
    // rest of the code
  }
  // more code
}
```

### 4.2 Prefer let and const

Use `let` and `const` instead of `var` for more predictable behavior and to avoid unintended hoisting issues.

```javascript
console.log(z); // ReferenceError: Cannot access 'z' before initialization
let z = 15;
console.log(z); // Output: 15
```

### 4.3 Prefer Function Declarations

For functions, use function declarations instead of function expressions for cleaner code and consistent hoisting behavior.

```javascript
greet(); // Output: 'Hello, World!'
function greet() {
  console.log('Hello, World!');
}
```
