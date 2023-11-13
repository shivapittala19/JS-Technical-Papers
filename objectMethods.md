# Title: Exploring Object Methods and Operations in JavaScript

## 1. Object Creation

### 1.1 Object Literal (Mutable)

Creates an object using the object literal notation.

```javascript
let person = { name: 'John', age: 30 };
```

### 1.2 Object.assign (Mutable)

Merges two or more objects into the target object.

```javascript
let person = { name: 'John', age: 30 };
let details = { occupation: 'developer', location: 'City' };

Object.assign(person, details);
console.log(person);
// Output: { name: 'John', age: 30, occupation: 'developer', location: 'City' }
```

### 1.3 Object.create (Immutable)

Creates a new object with the specified prototype object and properties.

```javascript
let person = { name: 'John', age: 30 };
let employee = Object.create(person, { occupation: { value: 'developer' } });

console.log(employee.name); // Output: 'John'
console.log(employee.occupation); // Output: 'developer'
```

## 2. Object Inspection

### 2.1 Object.keys (Immutable)

Returns an array of a given object's own enumerable property names.

```javascript
let person = { name: 'John', age: 30 };
let keys = Object.keys(person);
console.log(keys); // Output: ['name', 'age']
```

### 2.2 Object.values (Immutable)

Returns an array of a given object's own enumerable property values.

```javascript
let person = { name: 'John', age: 30 };
let values = Object.values(person);
console.log(values); // Output: ['John', 30]
```

### 2.3 Object.entries (Immutable)

Returns an array of a given object's own enumerable property `[key, value]` pairs.

```javascript
let person = { name: 'John', age: 30 };
let entries = Object.entries(person);
console.log(entries); // Output: [['name', 'John'], ['age', 30]]
```

## 3. Object Modification

### 3.1 Object.defineProperty (Mutable)

Adds or modifies a property on an object with the specified descriptor.

```javascript
let person = {};
Object.defineProperty(person, 'name', { value: 'John', writable: true });
console.log(person.name); // Output: 'John'
person.name = 'Jane';
console.log(person.name); // Output: 'Jane'
```

### 3.2 Object.freeze (Immutable)

Freezes an object, preventing new properties from being added, and existing properties from being modified or removed.

```javascript
let person = { name: 'John', age: 30 };
Object.freeze(person);
person.age = 31; // This operation is ignored in strict mode
console.log(person.age); // Output: 30 (unchanged)
```

### 3.3 Object.seal (Immutable)

Seals an object, preventing new properties from being added and marking all existing properties as non-configurable.

```javascript
let person = { name: 'John', age: 30 };
Object.seal(person);
delete person.age; // This operation is ignored
console.log(person.age); // Output: 30 (unchanged)
```

## 4. Object Deletion

### 4.1 delete Operator (Mutable)

Deletes a property from an object.

```javascript
let person = { name: 'John', age: 30 };
delete person.age;
console.log(person.age); // Output: undefined
```

## 5. Object Cloning

### 5.1 Object.assign (Mutable)

Creates a shallow copy of an object.

```javascript
let person = { name: 'John', age: 30 };
let clonedPerson = Object.assign({}, person);
console.log(clonedPerson); // Output: { name: 'John', age: 30 }
```

### 5.2 Spread Operator (Immutable)

Creates a shallow copy of an object using the spread operator.

```javascript
let person = { name: 'John', age: 30 };
let clonedPerson = { ...person };
console.log(clonedPerson); // Output: { name: 'John', age: 30 }
```
