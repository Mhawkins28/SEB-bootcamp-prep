# Functions and Control Flow Practice

The purpose of this exercise is to practice working with functions. Think of it as doing reps or practicing scales! The more you practice, the better you'll
get.

## Prerequisites

- Fundamental JavaScript: syntax, data types, and arrays
- Conditions, including `if`, `if`/`else`, and `if`/`else if`/`else`
- Loops, both `for` loops and `while` loops
- Function expressions

## Setup and Instructions

1. Create a javaScript file in your labs folder called `functions.js`, complete the excercies and `console.log` each exercise's answer.
2. Be sure to number each function with a comment above it.

- For example, here's the first function, our gift to you:

```js
// Exercise 1

const print = function (message) {
  console.log(message);
};

print("Hello, world!");
```

3. After completing each exercise, you may comment out that exercise's code to ease completion of subsequent exercises.

## Exercise

1. Define a function called `print`. It should take a parameter called `message`. When invoked and passed a string, `print` should `console.log` the message.

2. Define a function called `multiply` that takes two parameters: `a` and `b`. When invoked, return the product of `a` and `b`. If `b` is not passed, then return double `a` (i.e., multiply it by two). Store the returned value in a variable and log it to the terminal.

   > Hint: Use a default parameter.

3. Define a function called `maxOfTwoNumbers` that takes two numbers as arguments and returns the largest of them. If they are the same, return that number. Do not use the `Math.max` method.

4. Create a function called `greet` that takes a name as its parameter and returns a greeting message that says "Hello, [name]!"

5. Define a function called `sumArray` that takes an array of numbers and returns the sum of those numbers. Here’s how you can do it:

   - Initialize a variable `sum` to 0.
   - Use a `for` loop to iterate through each element of the array.
   - Add each element to `sum`.
   - Return `sum` after the loop ends.
     > Example: `sumArray([2, 4, 5]);` would return `11`.

6. Write a function called `calculateDifference` that takes two numbers and returns the absolute difference between them.

7. Create a function called `calculateAge` that takes a birth year as a parameter and returns the age based on the current year. Assume the current year is 2023.

8. Write a function called `containsTarget` that checks if an array contains a given target number. It should return true if the target exists in the array, otherwise false.

9. Using the following `nums` array, write a `for` loop to iterate through the `nums` array and add the number to one of the following arrays: `fizz`, `buzz`, or `fizzbuzz` - based upon the following:
   - Add to the `fizzbuzz` array if the number is evenly divisible by 3 & 5.
   - Add to the `fizz` array if the number is evenly divisible by 3.
   - Add to the `buzz` array if the number is evenly divisible by 5.

```js
const nums = [100, 5, 23, 15, 21, 72, 9, 45, 66, 7, 81, 90];
```

## Solution

Try not to peek!

<details>
<summary> 🔎 Possible Solutions</summary>

```js
// EXERCISE 1.
const print = function (message) {
  console.log(message);
};

// Example:
print("This is a test message.");

// EXERCISE 2.
const multiply = function (x, y = 2) {
  return x * y;
};

// Example:
console.log(multiply(5, 3)); // Output: 15
console.log(multiply(4)); // Output: 8

// EXERCISE 3.
const maxOfTwoNumbers = function (x, y) {
  if (x >= y) {
    return x;
  } else {
    return y;
  }
};

// Example:
console.log(maxOfTwoNumbers(5, 3)); // Output: 5
console.log(maxOfTwoNumbers(4, 7)); // Output: 7

// EXERCISE 4.
const greet = function (name) {
  return "Hello, " + name + "!";
};

// Example:
console.log(greet("Alice")); // Output: Hello, Alice!

// EXERCISE 5.
const sumArray = function (numbers) {
  let sum = 0;
  for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
  }
  return sum;
};

// Example:
console.log(sumArray([2, 4, 5])); // Output: 11

// EXERCISE 6.
const calculateDifference = function (num1, num2) {
  return Math.abs(num1 - num2);
};

// Example:
console.log(calculateDifference(10, 6)); // Output: 4

// EXERCISE 7.
const calculateAge = function (birthYear) {
  return 2023 - birthYear;
};

// Example:
console.log(calculateAge(1990)); // Output: 33

// EXERCISE 8.
const containsTarget = function (array, target) {
  return array.includes(target);
};

// Example:
console.log(containsTarget([1, 2, 3, 4, 5], 3)); // Output: true
console.log(containsTarget([1, 2, 3, 4, 5], 6)); // Output: false

// EXERCISE 9.
const fizz = [];
const buzz = [];
const fizzbuzz = [];

for (let i = 0; i < nums.length; i++) {
  const num = nums[i];
  if (num % 3 === 0 && num % 5 === 0) {
    fizzbuzz.push(num);
  } else if (num % 3 === 0) {
    fizz.push(num);
  } else if (num % 5 === 0) {
    buzz.push(num);
  }
}

console.log("fizz:", fizz);
console.log("buzz:", buzz);
console.log("fizzbuzz:", fizzbuzz);
```

</details>

## Additional Resources

- [MDN Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
