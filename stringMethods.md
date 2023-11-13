# Title: String Methods in JavaScript

## 1. Immutable String Methods

### 1.1 String.concat (Immutable)

Concatenates two or more strings, creating a new string without modifying the original strings.

```javascript
let greeting = 'Hello';
let modifiedGreeting = greeting.concat(', World!');
console.log(modifiedGreeting); // Output: 'Hello, World!'
console.log(greeting); // Output: 'Hello' (unchanged)
```

### 1.2 String.slice (Immutable)

Returns a shallow copy of a portion of a string into a new string.

```javascript
let sentence = 'This is a sample sentence';
let slicedSentence = sentence.slice(5, 10);
console.log(slicedSentence); // Output: 'is a '
console.log(sentence); // Output: 'This is a sample sentence' (unchanged)
```

### 1.3 String.substring (Immutable)

Returns a subset of a string between two specified indices into a new string.

```javascript
let phrase = 'JavaScript is amazing';
let subPhrase = phrase.substring(11, 18);
console.log(subPhrase); // Output: 'amazing'
console.log(phrase); // Output: 'JavaScript is amazing' (unchanged)
```

### 1.4 String.trim (Immutable)

Removes whitespace from both ends of a string and returns a new string.

```javascript
let paddedString = '   Trim me    ';
let trimmedString = paddedString.trim();
console.log(trimmedString); // Output: 'Trim me'
console.log(paddedString); // Output: '   Trim me    ' (unchanged)
```

## 2. Mutable String Methods

### 2.1 String.replace (Mutable)

Replaces a specified substring or pattern with another string.

```javascript
let sentence = 'JavaScript is fun!';
sentence = sentence.replace('fun', 'awesome');
console.log(sentence); // Output: 'JavaScript is awesome!'
```

### 2.2 String.toUpperCase (Mutable)

Converts all characters in a string to uppercase, modifying the original string.

```javascript
let lowercaseWord = 'hello';
lowercaseWord = lowercaseWord.toUpperCase();
console.log(lowercaseWord); // Output: 'HELLO'
```

### 2.3 String.toLowerCase (Mutable)

Converts all characters in a string to lowercase, modifying the original string.

```javascript
let uppercaseWord = 'WORLD';
uppercaseWord = uppercaseWord.toLowerCase();
console.log(uppercaseWord); // Output: 'world'
```

## 3. String Searching Methods

### 3.1 String.indexOf (Immutable)

Returns the index of the first occurrence of a specified value in a string.

```javascript
let sentence = 'JavaScript is powerful and versatile.';
let indexOfPowerful = sentence.indexOf('powerful');
console.log(indexOfPowerful); // Output: 13
console.log(sentence); // Output: 'JavaScript is powerful and versatile.' (unchanged)
```

### 3.2 String.includes (Immutable)

Checks if a string contains a specified value, returning true or false.

```javascript
let sentence = 'JavaScript is fun!';
let includesFun = sentence.includes('fun');
console.log(includesFun); // Output: true
console.log(sentence); // Output: 'JavaScript is fun!' (unchanged)
```

### 3.3 String.startsWith (Immutable)

Checks if a string starts with a specified value, returning true or false.

```javascript
let sentence = 'JavaScript is awesome!';
let startsWithJS = sentence.startsWith('JavaScript');
console.log(startsWithJS); // Output: true
console.log(sentence); // Output: 'JavaScript is awesome!' (unchanged)
```

### 3.4 String.endsWith (Immutable)

Checks if a string ends with a specified value, returning true or false.

```javascript
let sentence = 'JavaScript is incredible!';
let endsWithIncredible = sentence.endsWith('incredible');
console.log(endsWithIncredible); // Output: true
console.log(sentence); // Output: 'JavaScript is incredible!' (unchanged)
```

## 4. String Splitting and Joining Methods

### 4.1 String.split (Immutable)

Splits a string into an array of substrings based on a specified separator.

```javascript
let sentence = 'JavaScript is powerful and versatile.';
let words = sentence.split(' ');
console.log(words); // Output: ['JavaScript', 'is', 'powerful', 'and', 'versatile.']
console.log(sentence); // Output: 'JavaScript is powerful and versatile.' (unchanged)
```

### 4.2 Array.join (Immutable)

Joins the elements of an array into a string, separated by a specified separator.

```javascript
let words = ['JavaScript', 'is', 'powerful', 'and', 'versatile.'];
let joinedSentence = words.join(' ');
console.log(joinedSentence); // Output: 'JavaScript is powerful and versatile.'
console.log(words); // Output: ['JavaScript', 'is', 'powerful', 'and', 'versatile.'] (unchanged)
```