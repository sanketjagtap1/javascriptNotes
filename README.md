# Basics

## 1) Variables and Data Types:

   -    JavaScript is a loosely typed language, meaning variables can store any type of data without having to specify the type explicitly when the variable is declared. Variables are simply labels that store data, and the type of data they store can change during runtime. JavaScript has two primary categories of data types:

    - **i. Primitive Types**
    - **ii. Reference Types**

    -   Understanding these categories is essential to working with JavaScript effectively because each category behaves differently when assigned to variables, passed as arguments, or manipulated in various ways.

### **1. Primitive Types**

-  Primitive types are the simplest data types in JavaScript. They are immutable and hold a single value. When you assign a primitive value to a variable, the variable contains the actual value, and the value cannot be changed directly.

#### **i. String**

-    A string is a sequence of characters used to represent textual data.

-    Strings in JavaScript are immutable, meaning once they are created, they cannot be changed. Any modification to a string returns a new string, leaving the original unchanged.

```javascript
let name = "John";            // A simple string
let city = 'New York';        // A string using single quotes
let greeting = `Hello, ${name}!`; // Template literal (can include variables)
```

#### **ii. Number**

* A number is a numeric value that can be an integer or a floating-point number.

```javascript
let age = 30;            // An integer
let height = 1.75;       // A floating-point number
```

#### **iii. Boolean**

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

#### **v. Undefined**

* Undefined is a special value that represents an uninitialized variable.

```javascript
let username;             // An uninitialized variable
console.log(username);    // Output: undefined
```

#### **vi. BigInt**

* BigInt is a numeric value that can represent integers with arbitrary precision.

```javascript
let largeNumber = 12345678901234567890n; // A BigInt value
```

#### **vii. Symbol**

* Symbol is a unique and immutable value that can be used as a property key in objects.

```javascript
let uniqueKey = Symbol('uniqueKey'); // A Symbol value
```


### **1. Primitive Types**

    Reference type are more complex data structures. Unlike primitive types, reference type store the memory address (reference) to the actual value, meaning changes to the one reference variable affect the other variables that points to the same objects.

#### **i. Object:**

    * Objects are collection of key value pairs, where each key is a string (or symbol), and each value can be any data type, including other objects.

    ```javascript
        let person = {
        name: "Alice",
        age: 25,
        isActive: true,
        address: {
            street: "123 Main St",
            city: "Wonderland"
        }
        };
    ```

    * Objects can be created using the object literal {} or the new object() syntax. Accessing object properties:

    * Dot Operator
