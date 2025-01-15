# Accessing Nested Data Structures in JavaScript

## Introduction

In JavaScript, it's common to encounter data structures where objects and arrays are nested within each other. This setup can help organize complex data more effectively. Learning how to access nested data is crucial for manipulating these data structures efficiently.

## Nested Data Structure Example

Consider the following example of a nested data structure which includes an array of objects, each containing arrays or objects themselves:

**Example:**

```javascript
const school = {
  name: "Greenwood High",
  classes: [
    {
      name: "Grade 1",
      students: [
        { name: "John Doe", age: 6 },
        { name: "Jane Doe", age: 7 },
      ],
    },
    {
      name: "Grade 2",
      students: [
        { name: "Alice Johnson", age: 7 },
        { name: "Bob Smith", age: 8 },
      ],
    },
  ],
};
```

## Practice: Accessing Nested Data

Let's practice accessing various parts of this nested data structure.

### Task 1: Access the name of the school

<details>
<summary>Solution</summary>

```javascript
console.log(school.name); // Outputs: "Greenwood High"
```

</details>

### Task 2: Access the array of students in "Grade 1"

<details>
<summary>Solution</summary>

```javascript
console.log(school.classes[0].students); // Outputs the students array in Grade 1
```

</details>

### Task 3: Access the name of the first student in "Grade 2"

<details>
<summary>Solution</summary>

```javascript
console.log(school.classes[1].students[0].name); // Outputs: "Alice Johnson"
```

</details>

### Task 4: Change the age of Jane Doe to 8

<details>
<summary>Solution</summary>

```javascript
school.classes[0].students[1].age = 8;
console.log(school.classes[0].students[1]); // Outputs: { name: "Jane Doe", age: 8 }
```

</details>

## Conclusion

Working with nested data structures involves understanding how to access each layer of the structure using a combination of dot notation and array indexing. Practice with these structures will help you navigate and manipulate even the most complex data in your JavaScript applications.
