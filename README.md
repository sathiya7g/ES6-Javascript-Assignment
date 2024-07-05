# ES6-Javascript-Assignment

1)Create two variables using let and const. The let variable should be named age and set to 30. The const variable should be named name and set to "Alice". Try to reassign the name variable and observe what happens.

**coding:**
```
let age = 30;
const name = "Alice";
console.log(age); 
console.log(name);

try {
    name = "Bob";
} catch (error) {
    console.error(error); 
}
```
**Output:**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20060021.png)

**Exercise 2: Arrow Functions**

**Problem Statement:**

Convert the following function into an arrow function.

function add(a, b) {

return a + b;

}

Hint/Explanation:

Arrow functions provide a concise syntax and lexically bind the this value.

Solution:

const add = (a, b) => a + b;

**coding**
```
function add(a, b) {
    return a + b;
}

const addArrow = (a, b) => a + b;

console.log(add(2, 3));      
console.log(addArrow(5, 3)); 
```
**Output:**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20063130.png)

**Exercise 3: Template Literals**
**Problem Statement:**

Use a template literal to print "Hello, Alice! Your age is 30." using the variables name and age.

Hint/Explanation:

Template literals allow embedded expressions and multi-line strings.

Solution:

console.log(`Hello, ${name}! Your age is ${age}.`);

**coding**
```
const name = "Alice";
let age = 30;

console.log(`Hello, ${name}! Your age is ${age}.`);
```
**Output:**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20063458.png)

**Exercise 4: Destructuring Objects**
**Problem Statement:**

Given an object { firstName: "Alice", lastName: "Johnson" }, use object destructuring to extract firstName and lastName into variables.

Hint/Explanation:

Destructuring allows you to unpack values from arrays or properties from objects.

Solution:

const person = { firstName: "Alice", lastName: "Johnson" };

const { firstName, lastName } = person;

**coding**

const person = { firstName: "Alice", lastName: "Johnson" };

const { firstName, lastName } = person;

console.log(firstName); 
console.log(lastName);  

**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20064720.png)

**Exercise 5: Destructuring Arrays**
**Problem Statement:**

Given an array [1, 2, 3, 4, 5], use array destructuring to create variables first and second for the first two elements.

Hint/Explanation:

Array destructuring works similarly to object destructuring but with array elements.

Solution:

const numbers = [1, 2, 3, 4, 5];

const [first, second] = numbers;

**coding**
const numbers = [1, 2, 3, 4, 5];

const [first, second] = numbers;

console.log(first);  
console.log(second); 

**output**
![image](
