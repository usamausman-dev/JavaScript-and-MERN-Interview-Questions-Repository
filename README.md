
# JavaScript and MERN Interview Questions Repository

Welcome to the JavaScript and MERN Interview Questions Repository. This GitHub project is dedicated to providing a curated collection of interview questions specifically tailored to JavaScript developers and those working with the MERN (MongoDB, Express.js, React, Node.js) stack. Whether you're gearing up for a JavaScript-focused interview or seeking MERN-related positions, you'll find a wealth of questions and resources here to boost your preparation. Contribute your questions and insights to help fellow developers excel in their interviews. Dive in, master the essentials, and land your dream job in the world of JavaScript and MERN development!

## Questions


### Questions-1: 
What are the key differences between var, let, and const when declaring variables in JavaScript, and when would you use each of them?

#### Answer : 
In JavaScript, var, let, and const are used to declare variables, but they differ in their behavior and use cases:



|     | var | let    | const |
| --------- | ------- |--------- | ------- |
|Scope|  Variables declared with var are function-scoped, meaning they are only accessible within the function in which they are defined. |Variables declared with let are block-scoped, meaning they are only accessible within the block (e.g., inside curly braces) in which they are defined. | Variables declared with const are block-scoped, just like let.
| Hoisting| Variables declared with var are hoisted to the top of their function or global scope. This means you can use them before they are declared, but they will have an initial value of undefined. |Like var, variables declared with let are hoisted, but they are not initialized, so accessing them before declaration results in a ReferenceError.|Like let, const variables are hoisted but not initialized. Accessing them before declaration results in a ReferenceError.|
| Reassignment| You can reassign values to variables declared with var. | You can reassign values to variables declared with let.|Variables declared with const cannot be reassigned once they are given a value. However, for objects and arrays declared with const, you can still modify their properties or elements.|

#### Example: 
```javascript
function exampleVar() {
  if (true) {
    var x = 10;
  }
  console.log(x); // Outputs 10
}

function exampleLet() {
  if (true) {
    let y = 20;
  }
  console.log(y); // Throws ReferenceError: y is not defined
}


function exampleConst() {
  if (true) {
    const z = 30;
  }
  console.log(z); // Throws ReferenceError: z is not defined
}


```

### Questions-2:
Difference between Arrow Function & Normal Function

###### Answer :

| Aspect                           | Arrow Functions                     | Normal Functions               |
|----------------------------------|-------------------------------------|-------------------------------|
| Syntax                           | `(params) => expression`            | `function name(params) {...}` |
| `this` Binding                   | Lexical (bound to enclosing scope)  | Dynamic (depends on caller)   |
| Arguments Object                 | No                                  | Yes (available)               |
| `arguments` Variable             | No                                  | Yes (available)               |
| Constructor Function             | No                                  | Yes (can be used)             |
| Use in Methods                   | Not suitable for object methods     | Suitable for object methods   |
| Use in Callbacks                 | Concise and readable                | Commonly used                  |
| Clarity and Conciseness          | Concise and often more readable     | May be verbose                |
| Best for                        | Short, simple functions             | Complex functions or methods  |

#### Arrow Functions Example

```javascript
const add = (a, b) => a + b;
const double = (n) => n * 2;

// Usage
console.log(add(2, 3));      // 5
console.log(double(4));      // 8

```

#### Normal Functions Example

```javascript
function add(a, b) {
  return a + b;
}

function double(n) {
  return n * 2;
}

// Usage
console.log(add(2, 3));      // 5
console.log(double(4));      // 8


```

