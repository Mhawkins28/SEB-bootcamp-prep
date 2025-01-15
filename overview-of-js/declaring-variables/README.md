# Variables in JavaScript

## Introduction

Variables are fundamental in any programming language. They act as containers for storing data values. In JavaScript, the creation and management of variables is straightforward yet governed by specific rules which enhance the language's flexibility and functionality.

## Variable Foundation

The purpose of a variable in programming is to hold or reference data. Variables are created using a declaration keyword followed by an identifier and an assignment operator to set its value.

### Components of a Variable Declaration

- **Declaration Keyword**: Commonly `let` or `const`.
- **Identifier**: The variable name, e.g., `nameVariable`.
- **Assignment Operator**: `=`
- **Stored Data**: The data assigned to the variable, e.g., `"Tony Stark"`.

A variable declaration can end with an optional semicolon.

Example of declaring a variable:

```javascript
let nameVariable = "Tony Stark";
```

> Note:
> While you decide what the identifier is named, there are naming conventions and rules you must follow!

## Variable Declarations & Rules

Creating variables in JavaScript requires understanding the use of `let` and `const`. These keywords are known as declarations and are followed by the variable's name.

### let vs const

- `let` allows you to declare a variable with the option to reassign its value later.
- `const` is used for declaring variables whose values are not meant to be changed once set.

```javascript
let age = 30;
age = 31; // valid

const birthYear = 1991;
birthYear = 1992; // This will cause an error
```

## Naming Rules for Variables

When naming variables, it's important to adhere to the following rules:

- **Characters**: Use letters (e.g., a, b, c).
- **Numbers**: Can be included but not as the first character.
- **Dollar Sign ($)** and **Underscore (\_)**
- **Case Sensitivity**: Variable names are case-sensitive.

### Invalid Naming Conventions

- Special characters (other than $ and \_)
- Spaces or single-dashes "-"
- Starting with a number

### Naming Convention

In JavaScript, the convention is to use `lowerCamelCase` for identifiers:

- Multi-word variables: `numActivePlayers`, `tacoFlavor09`, `isRunning`
- Single-word variables: `_data`, `$message`, `toys`

### Examples

```javascript
let userName = "JohnDoe"; // Correctly using lowerCamelCase
const eyeColor = "brown"; // Correctly declared with const because the eye color likely won't change
let num1 = 10 // Correctly declared

// Improperly written variables
let user-name = "Sarah"; // Incorrect: hyphens are not allowed in variable names
let 1num = 10 // Incorrect: Although you can use numbers for variable naming, it can't start with a number

// Examples of variable names with special characters or spaces
let user address = "123 Fake St"; // Incorrect: spaces are not allowed
let user#id = 101; // Incorrect: hash (#) is a special character and is not allowed

// More examples of correct variable naming
let $element = $("#element"); // Correct if using jQuery, where $ indicates a jQuery object
let _tempVar = "temporary"; // Correct: underscores are allowed and often used for temporary or private variables

// Examples using camelCase
let numberOfUsers = 10; // Correct: clear and descriptive
let menuBackgroundColor = "blue"; // Correct: descriptive multi-word variable using camelCase
```

## Conclusion

Understanding how to declare and name variables correctly in JavaScript is crucial for writing clear and maintainable code. Remember these guidelines as you start to write more complex programs.
