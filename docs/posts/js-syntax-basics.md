---
draft: false
date: 2024-07-12
authors:
  - hcoco1
categories:
  - Javascript
  - Web Development
---

# JavaScript Basics

![alt text](https://images.unsplash.com/photo-1667372393096-9c864313e868?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

JavaScript, often abbreviated JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. It lets us add interactivity to pages e.g. you might have seen sliders, alerts, click interactions, popups, etc on different websites — all of that is built using JavaScript...


<!-- more -->

## 1. Syntax and Basics

### 1.1 Variables: `var`, `let`, `const`

#### Explanation:

- `var`: Variable declared using `var` can be redeclared and reassigned. It has function scope.
- `let`: Variable declared using `let` can be reassigned but not redeclared in the same scope. It has block scope.
- `const`: Variable declared using `const` cannot be reassigned or redeclared. It must be initialized at the time of declaration and has block scope.

In JavaScript, `let`, `const`, and `var` are used to declare variables. `var` is function-scoped and has been the traditional way of declaring variables. `let` and `const` are block-scoped, and they were introduced in ECMAScript 2015 (ES6).

`let` allows you to declare a variable that can be reassigned, while `const` is used to declare a variable that cannot be reassigned.


#### Question 1: Variable Declaration
Declare three variables: one using `var`, one using `let`, and one using `const`. Assign any value to each variable and log them to the console.

```javascript
var x = 10;
let y = 20;
const z = 30;

console.log(x); // 10
console.log(y); // 20
console.log(z); // 30
```

#### Question 2: Variable Reassignment
Try reassigning the variables declared in the previous question. Note any differences in behavior.

```javascript
x = 15;
y = 25;
// z = 35; // Uncommenting this line will throw an error because 'const' variables cannot be reassigned.

console.log(x); // 15
console.log(y); // 25
// console.log(z); // 30
```

### 1.2 Data Types

#### Explanation:
JavaScript supports several data types including:

- **String**: A sequence of characters, e.g., `"Hello"`
- **Number**: Any numeric value, e.g., `42`
- **Boolean**: Logical values, `true` or `false`
- **Array**: An ordered collection of values, e.g., `[1, 2, 3]`
- **Object**: A collection of key-value pairs, e.g., `{ name: "John", age: 30 }`

#### Question 3: Data Types Identification
Create variables of different data types: string, number, boolean, array, and object. Log the type of each variable using `typeof`.

```javascript
let str = "Hello";
let num = 42;
let bool = true;
let arr = [1, 2, 3];
let obj = { name: "John", age: 30 };

console.log(typeof str); // "string"
console.log(typeof num); // "number"
console.log(typeof bool); // "boolean"
console.log(typeof arr); // "object"
console.log(typeof obj); // "object"
```

### 1.3 Operators

#### Explanation:
Operators are used to perform operations on variables and values:

- **Arithmetic Operators**: `+`, `-`, `*`, `/`
- **Comparison Operators**: `>`, `<`, `>=`, `<=`, `===`, `!==`
- **Logical Operators**: `&&` (AND), `||` (OR), `!` (NOT)

#### Question 4: Arithmetic Operators
Perform arithmetic operations (addition, subtraction, multiplication, division) on two numbers and log the results.

```javascript
let a = 10;
let b = 5;

console.log(a + b); // 15
console.log(a - b); // 5
console.log(a * b); // 50
console.log(a / b); // 2
```

#### Question 5: Comparison Operators
Compare two numbers using comparison operators (>, <, >=, <=, ===, !==) and log the results.

```javascript
let a = 10;
let b = 5;

console.log(a > b); // true
console.log(a < b); // false
console.log(a >= b); // true
console.log(a <= b); // false
console.log(a === b); // false
console.log(a !== b); // true
```

#### Question 6: Logical Operators
Use logical operators (&&, ||, !) on two boolean values and log the results.

```javascript
let bool1 = true;
let bool2 = false;

console.log(bool1 && bool2); // false
console.log(bool1 || bool2); // true
console.log(!bool1); // false
```

## 2. Control Structures

### 2.1 Conditional Statements

#### Explanation:
Conditional statements are used to perform different actions based on different conditions:
- `if`: Executes a block of code if a specified condition is true.
- `else`: Executes a block of code if the same condition is false.
- `else if`: Specifies a new condition to test if the first condition is false.
- `switch`: Specifies many alternative blocks of code to be executed.

#### Question 7: `if`, `else`, `else if`
Write a function that takes a number as input and logs whether the number is positive, negative, or zero.

```javascript
function checkNumber(num) {
    if (num > 0) {
        console.log("Positive");
    } else if (num < 0) {
        console.log("Negative");
    } else {
        console.log("Zero");
    }
}

checkNumber(5);   // Positive
checkNumber(-3);  // Negative
checkNumber(0);   // Zero
```

### 2.2 Loops

#### Explanation:
Loops are used to execute a block of code multiple times:
- `for`: Loops through a block of code a number of times.
- `while`: Loops through a block of code as long as a specified condition is true.
- `do...while`: Also loops through a block of code as long as a specified condition is true, but it will execute the block of code once before checking the condition.

#### Question 8: `for` Loop
Write a `for` loop that logs numbers from 1 to 10.

```javascript
for (let i = 1; i <= 10; i++) {
    console.log(i);
}
```

#### Question 9: `while` Loop
Write a `while` loop that logs numbers from 10 to 1.

```javascript
let i = 10;
while (i > 0) {
    console.log(i);
    i--;
}
```

#### Question 10: `do...while` Loop
Write a `do...while` loop that logs numbers from 1 to 5.

```javascript
let i = 1;
do {
    console.log(i);
    i++;
} while (i <= 5);
```

## 3. Functions

### 3.1 Function Declaration and Invocation

#### Explanation:
A function is a block of code designed to perform a particular task. It is executed when "called" (invoked).
- **Function Declaration**: Defines a function using the `function` keyword.
- **Function Invocation**: Executes the function by calling it with parentheses.

#### Question 11: Function Declaration and Invocation
Declare a function that takes two numbers as arguments and returns their sum. Invoke the function with two numbers and log the result.

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(5, 7)); // 12
```

### 3.2 Parameters and Return Values

#### Explanation:
Functions can take parameters (inputs) and return a value. The `return` statement stops the execution of the function and returns a value.

#### Question 12: Parameters and Return Values
Write a function that takes an array as a parameter and returns the sum of its elements.

```javascript
function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

console.log(sumArray([1, 2, 3, 4])); // 10
```

### 3.3 Arrow Functions

#### Explanation:
Arrow functions provide a shorter syntax for writing functions. They are always anonymous.

```javascript
// Traditional Function
function add(a, b) {
    return a + b;
}

// Arrow Function
const add = (a, b) => a + b;
```

#### Question 13: Arrow Functions
Rewrite the function from Question 12 using arrow function syntax.

```javascript
const sumArray = (arr) => {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

console.log(sumArray([1, 2, 3, 4])); // 10
```

This set of coding questions covers the basics of JavaScript, including variable declarations, data types, operators, control structures, and functions. These questions aim to help you understand and practice the fundamental concepts of JavaScript.