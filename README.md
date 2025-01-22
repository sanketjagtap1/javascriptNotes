# Basics

1) Variables and Data Types:

    JavaScript is a loosely typed language, meaning variables can store any type of data without having to specify the type explicitly when the variable is declared. Variables are simply labels that store data, and the type of data they store can change during runtime. JavaScript has two primary categories of data types:

    i. Primitive Types
    ii. Reference Types

    Understanding these categories is essential to working with JavaScript effectively because each category behaves differently when assigned to variables, passed as arguments, or manipulated in various ways.

### 1. Primitive Types

Primitive types are the simplest data types in JavaScript. They are immutable and hold a single value. When you assign a primitive value to a variable, the variable contains the actual value, and the value cannot be changed directly.

#### i. String

* A string is a sequence of characters used to represent textual data.
* Strings in JavaScript are immutable, meaning once they are created, they cannot be changed. Any modification to a string returns a new string, leaving the original unchanged.

```javascript
let name = "John";            // A simple string
let city = 'New York';        // A string using single quotes
let greeting = `Hello, ${name}!`; // Template literal (can include variables)
```

#### ii. Number

* A number is a numeric value that can be an integer or a floating-point number.

```javascript
let age = 30;            // An integer
let height = 1.75;       // A floating-point number
```

#### iii. Boolean

* A boolean is a logical value that can be either true or false.

```javascript
let isAdmin = true;       // A boolean value
let isGuest = false;      // Another boolean value
```

#### iv. Null

* Null is a special value that represents the absence of any object value.

```javascript
let user = null;          // A null value
```

#### v. Undefined

* Undefined is a special value that represents an uninitialized variable.

```javascript
let username;             // An uninitialized variable
console.log(username);    // Output: undefined
```

#### vi. BigInt

* BigInt is a numeric value that can represent integers with arbitrary precision.

```javascript
let largeNumber = 12345678901234567890n; // A BigInt value
```

#### vii. Symbol

* Symbol is a unique and immutable value that can be used as a property key in objects.

```javascript
let uniqueKey = Symbol('uniqueKey'); // A Symbol value
```
```javascript
// Reference Types
// Reference types are more complex data structures. Unlike primitive types, reference types store the memory address (reference) to the actual value, meaning changes to one reference variable can affect other variables that point to the same object.

// A. Object
// Objects are collections of key-value pairs, where each key is a string (or Symbol), and each value can be any data type, including other objects.
/**
 * Example of an object
 */
let person = {
  name: "Alice",
  age: 25,
  isActive: true,
  address: {
    street: "123 Main St",
    city: "Wonderland"
  }
};

// Objects can be created using the object literal {} or the new Object() syntax.
// Accessing object properties:
// Using dot notation:
console.log(person.name);  // Alice
// Using bracket notation:
console.log(person["age"]);  // 25

// Objects are mutable, meaning properties can be added, modified, or removed after creation.
// Example:
person.age = 30;            // Modify a property
person.country = "USA";     // Add a new property
delete person.isActive;    // Remove a property

// B. Array
// An array is a special type of object used to store ordered collections of values (elements). Arrays can hold multiple types of data, including other arrays or objects.
/**
 * Example of an array
 */
let colors = ["red", "green", "blue"];
let numbers = [1, 2, 3, 4];

// Arrays are accessed using index positions (starting from 0).
console.log(colors[0]);  // red

// Arrays are mutable, meaning you can change elements, add new elements, or remove elements.
colors[1] = "yellow";  // Modifies the second element
colors.push("purple");  // Adds a new element at the end

// Arrays have built-in methods like .map(), .filter(), .forEach(), etc., for manipulating elements.

// C. Function
// A function is a block of code designed to perform a particular task. Functions in JavaScript are first-class objects, meaning they can be assigned to variables, passed as arguments, or returned from other functions.
/**
 * Example of a function
 */
function add(a, b) {
  return a + b;
}

console.log(add(5, 3));  // 8

// Functions are invoked by calling their name with parentheses and arguments, if needed.
function greet(name) {
  console.log("Hello, " + name);
}

greet("John");  // Hello, John

// Anonymous functions: Functions can also be declared without a name (used mostly as arguments for other functions).
setTimeout(function() {
  console.log("This runs after 2 seconds");
}, 2000);

// Arrow functions (introduced in ES6) provide a concise way to define functions.
const addArrow = (a, b) => a + b;

// Summary of Differences Between Primitive Types and Reference Types
// Feature	Primitive Types	Reference Types
// Storage	Stores the actual value	Stores a reference (memory address) to the value
// Mutability	Immutable (cannot be changed directly)	Mutable (can be modified)
// Assignment	Copies the value (pass-by-value)	Copies the reference (pass-by-reference)
// Example	string, number, boolean, null, undefined, symbol	object, array, function
// Equality	Compared by value	Compared by reference
```
