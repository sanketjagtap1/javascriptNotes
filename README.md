
# Basics

## 1) Variables and Data Types:

JavaScript is a loosely typed language, meaning variables can store any type of data without having to specify the type explicitly when the variable is declared. Variables are simply labels that store data, and the type of data they store can change during runtime. JavaScript has two primary categories of data types:

-    **i. Primitive Types**
-    **ii. Reference Types**

Understanding these categories is essential to working with JavaScript effectively because each category behaves differently when assigned to variables, passed as arguments, or manipulated in various ways.

### **1. Primitive Types**
---
Primitive types are the simplest data types in JavaScript. They are immutable and hold a single value. When you assign a primitive value to a variable, the variable contains the actual value, and the value cannot be changed directly.

#### **i. String**

-    A string is a sequence of characters used to represent textual data.

-    Strings in JavaScript are immutable, meaning once they are created, they cannot be changed. Any modification to a string returns a new string, leaving the original unchanged.

```javascript
let name = "John";            // A simple string
let city = 'New York';        // A string using single quotes
let greeting = `Hello, ${name}!`; // Template literal (can include variables)
```

#### **ii. Number**

- A number is a numeric value that can be an integer or a floating-point number.

```javascript
let age = 30;            // An integer
let height = 1.75;       // A floating-point number
```

#### **iii. Boolean**

- A boolean is a logical value that can be either true or false.

```javascript
let isAdmin = true;       // A boolean value
let isGuest = false;      // Another boolean value
```

#### **iv. Null**

- Null is a special value that represents the absence of any object value.

```javascript
let user = null;          // A null value
```

#### **v. Undefined**

- Undefined is a special value that represents an uninitialized variable.

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


### **1. Reference/Non-primitive Types:**

Reference type are more complex data structures. Unlike primitive types, reference type store the memory address (reference) to the actual value, meaning changes to the one reference variable affect the other variables that points to the same objects.

#### **i. Object:**

- Objects are collection of key value pairs, where each key is a string (or symbol), and each value can be any data type, including other objects.

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

* Using dot notation:
    ```javascript
    console.log(person.name);  // Alice
    ```

* Using bracket notation:
    ```javascript
    console.log(person['name']);  // Alice
    ```

* Object are mutable, meaning objects can be added, modified or removed after creation.

    ```javascript
    person.age = 30;            // Modify a property
    person.country = "USA";     // Add a new property
    delete person.isActive;    // Remove a property
    ```

### **ii. Array :**

- An array is a special type of object used to store ordered collection of **values (elements)**. Array can store multiple types of data including other type of objects or arrays.

- Array are accessed using **index position** (Starting from 0).

    ```javascript
    let colors = ["red", "yellow", 3, 4];
    console.log(data[1]) // yellow
    ```

- Arrays are mutable, meaning you can add, modify or remove the values after creation.

#### Example: 
```javascript
    colors[1] = "yellow";  // Modifies the second element
    colors.push("purple");  // Adds a new element at the end
```

- Arrays have built in methods like .map(), .filter(), etc for manipulating elements.

### **c. Functions:**

- A function is a block of code design to perform the particular task. Function in javascript are first class objects, meaning they can be assigned to variables, passed as arguments, or return from another function.

```javascript
    function add(a, b){
        return a + b;
    }

    console.log(add(4+4)) // 8
```

- Functions are invoked by calling there name with () parentheses and arguments if required.

#### Example:
```javascript
    function greet(name) {
        console.log("Hello, " + name);
    }

    greet("John");  // Hello, John
```

## **Differences Between Primitive Types and Reference Types:**

| Feature       | Primitive Types                        | Reference Types                        |
|---------------|----------------------------------------|----------------------------------------|
| **Storage**   | Stores the actual value                | Stores a reference (memory address) to the value |
| **Mutability**| Immutable (cannot be changed directly) | Mutable (can be modified)              |
| **Assignment**| Copies the value (pass-by-value)      | Copies the reference (pass-by-reference) |
| **Example**   | string, number, boolean, null, undefined, symbol | object, array, function              |
| **Equality**  | Compared by value                      | Compared by reference                  |

 

---
# Operators in JavaScript
---

In JavaScript, operators are special symbols or keywords that are used to perform operations on values and variables. These operations include mathematical calculations, comparisons, logical operations, and more. The following is a breakdown of the different types of operators available in JavaScript.

---

## 1. **Arithmetic Operators**

Arithmetic operators are used to perform basic mathematical operations.

- **`+` (Addition)**: Adds two operands.
  - Example: 
    ```javascript
    let sum = 5 + 3;  // sum equals 8
    ```

- **`-` (Subtraction)**: Subtracts the right operand from the left operand.
  - Example: 
    ```javascript
    let diff = 5 - 3;  // diff equals 2
    ```

- **`*` (Multiplication)**: Multiplies two operands.
  - Example: 
    ```javascript
    let product = 5 * 3;  // product equals 15
    ```

- **`/` (Division)**: Divides the left operand by the right operand.
  - Example:
    ```javascript
    let quotient = 5 / 3;  // quotient equals 1.6667
    ```

- **`%` (Modulo)**: Returns the remainder of the division.
  - Example:
    ```javascript
    let remainder = 5 % 3;  // remainder equals 2
    ```

- **`++` (Increment)**: Increases the value of a variable by 1.
  - Example:
    ```javascript
    let x = 5;
    x++;  // x becomes 6
    ```

- **`--` (Decrement)**: Decreases the value of a variable by 1.
  - Example:
    ```javascript
    let x = 5;
    x--;  // x becomes 4
    ```

---

## 2. **Comparison Operators**

Comparison operators are used to compare two values, returning a boolean value (`true` or `false`).

- **`==` (Equal to)**: Returns `true` if the operands are equal (performs type coercion).
  - Example:
    ```javascript
    5 == '5';  // true, because '5' is coerced to the number 5
    ```

- **`===` (Strict Equal to)**: Returns `true` if the operands are equal and of the same type (no type coercion).
  - Example:
    ```javascript
    5 === '5';  // false, because one is a number and the other is a string
    ```

- **`!=` (Not equal to)**: Returns `true` if the operands are not equal (performs type coercion).
  - Example:
    ```javascript
    5 != '5';  // false, because '5' is coerced to the number 5
    ```

- **`!==` (Strict Not Equal to)**: Returns `true` if the operands are not equal or not of the same type.
  - Example:
    ```javascript
    5 !== '5';  // true, because the types are different
    ```

- **`>` (Greater than)**: Returns `true` if the left operand is greater than the right operand.
  - Example:
    ```javascript
    5 > 3;  // true
    ```

- **`<` (Less than)**: Returns `true` if the left operand is less than the right operand.
  - Example:
    ```javascript
    5 < 3;  // false
    ```

- **`>=` (Greater than or equal to)**: Returns `true` if the left operand is greater than or equal to the right operand.
  - Example:
    ```javascript
    5 >= 3;  // true
    ```

- **`<=` (Less than or equal to)**: Returns `true` if the left operand is less than or equal to the right operand.
  - Example:
    ```javascript
    5 <= 3;  // false
    ```

---

## 3. **Logical Operators**

Logical operators are used to combine multiple boolean expressions and return a boolean value.

- **`&&` (Logical AND)**: Returns `true` if both operands are `true`.
  - Example:
    ```javascript
    true && false;  // false
    ```

- **`||` (Logical OR)**: Returns `true` if at least one of the operands is `true`.
  - Example:
    ```javascript
    true || false;  // true
    ```

- **`!` (Logical NOT)**: Reverses the boolean value of the operand.
  - Example:
    ```javascript
    !true;  // false
    ```

---

## 4. **Bitwise Operators**

Bitwise operators operate on the binary representations of numbers.

- **`&` (AND)**: Performs a bitwise AND operation on two numbers.
  - Example:
    ```javascript
    5 & 3;  // 1 (binary: 101 & 011 = 001)
    ```

- **`|` (OR)**: Performs a bitwise OR operation on two numbers.
  - Example:
    ```javascript
    5 | 3;  // 7 (binary: 101 | 011 = 111)
    ```

- **`^` (XOR)**: Performs a bitwise XOR (exclusive OR) operation.
  - Example:
    ```javascript
    5 ^ 3;  // 6 (binary: 101 ^ 011 = 110)
    ```

- **`~` (NOT)**: Inverts the bits of a number.
  - Example:
    ```javascript
    ~5;  // -6 (binary: ~00000101 = 11111010)
    ```

- **`<<` (Left Shift)**: Shifts the bits of a number to the left.
  - Example:
    ```javascript
    5 << 1;  // 10 (binary: 101 << 1 = 1010)
    ```

- **`>>` (Right Shift)**: Shifts the bits of a number to the right.
  - Example:
    ```javascript
    5 >> 1;  // 2 (binary: 101 >> 1 = 10)
    ```

- **`>>>` (Unsigned Right Shift)**: Shifts the bits to the right, filling the leftmost bits with zeros.
  - Example:
    ```javascript
    -5 >>> 1;  // large positive number because of sign extension
    ```

---

## 5. **Assignment Operators**

Assignment operators are used to assign values to variables.

- **`=` (Assignment)**: Assigns the right operand's value to the left operand.
  - Example:
    ```javascript
    let x = 5;
    ```

- **`+=` (Addition Assignment)**: Adds the right operand to the left operand and assigns the result to the left operand.
  - Example:
    ```javascript
    let x = 5;
    x += 3;  // x becomes 8
    ```

- **`-=` (Subtraction Assignment)**: Subtracts the right operand from the left operand and assigns the result to the left operand.
  - Example:
    ```javascript
    let x = 5;
    x -= 3;  // x becomes 2
    ```

- **`*=` (Multiplication Assignment)**: Multiplies the left operand by the right operand and assigns the result to the left operand.
  - Example:
    ```javascript
    let x = 5;
    x *= 3;  // x becomes 15
    ```

- **`/=` (Division Assignment)**: Divides the left operand by the right operand and assigns the result to the left operand.
  - Example:
    ```javascript
    let x = 5;
    x /= 3;  // x becomes 1.6667
    ```

- **`%=` (Modulo Assignment)**: Assigns the remainder of the division of the left operand by the right operand to the left operand.
  - Example:
    ```javascript
    let x = 5;
    x %= 3;  // x becomes 2
    ```

---

## 6. **Ternary Operator**

The ternary operator is a shorthand way to write
