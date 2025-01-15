# Data Types Overview in JavaScript

## Introduction

Variables in JavaScript can store various types of data, which are broadly categorized into primitive and non-primitive data types. Understanding these data types is foundational for programming in JavaScript, as it influences how data can be manipulated and used effectively.

## Primitive Data Types

Primitive data types include:

- **String**
- **Number**
- **Boolean**
- **Undefined**
- **Null**

### String

Strings are sequences of characters used for storing text. They can be enclosed in single quotes (`'`), double quotes (`"`), or backticks (`` ` ``) for template literals. Convention is to use double quotes in most cases.

**Example:**

```javascript
let greeting = "Hello, world!";
let response = "Hi there!";
console.log(typeof greeting); // Outputs: string
```

### Number

Numbers represent both integer and floating-point numbers in JavaScript. Unlike some other languages, there is no separate type for integers.

**Example:**

```javascript
let age = 25;
let price = 99.95;
console.log(typeof age); // Outputs: number
```

### Boolean

Booleans represent a logical entity and can have two values: `true` and `false`.

**Example:**

```javascript
let isApproved = true;
let isFinished = false;
console.log(typeof isApproved); // Outputs: boolean
```

### Undefined

A variable that has not been assigned a value is of type undefined.

**Example:**

```javascript
let name;
console.log(typeof name); // Outputs: undefined
```

### Null

Null is a special type that represents "no value" or "nothing". It's important to note that `typeof` `null` will return `"object"`, which is a well-known JavaScript peculiarity. Which is why we simply do not use null.

**Example:**

```javascript
let empty = null;
console.log(typeof empty); // Outputs: object (This is a JS bug!)
```

## Non-Primitive Data Types

Non-primitive types are used to store collections of data and more complex entities (to be covered in depth in the following lessons).

- Object
- Array

### Object

Objects represent collections of properties, which can be defined as key-value pairs.

**Example:**

```javascript
let user = {
  name: "John",
  age: 30,
};
console.log(typeof user); // Outputs: object
```

### Array

Arrays are a type of object used for storing multiple values in a single variable.

**Example:**

```javascript
let colors = ["Red", "Blue", "Green"];
console.log(typeof colors); // Outputs: object
console.log(Array.isArray(colors)); // Outputs: true (to check if it's an array)
```

## Conclusion

JavaScript provides a range of data types that allow you to manipulate data in various ways. Understanding these types will help you decide how to structure your data in programs and how you can interact with it.

In the next lessons, we will cover Objects and Arrays, the non-primitive data-types, more closely.
