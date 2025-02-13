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
```
const person = { firstName: "Alice", lastName: "Johnson" };

const { firstName, lastName } = person;

console.log(firstName); 
console.log(lastName);  
```
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
```
const numbers = [1, 2, 3, 4, 5];

const [first, second] = numbers;

console.log(first);  
console.log(second); 
```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20065208.png)

**Exercise 6: Spread Operator**
**Problem Statement:**

Combine two arrays [1, 2, 3] and [4, 5, 6] into a new array using the spread operator.

Hint/Explanation:

The spread operator allows an iterable (like an array) to be expanded in places where zero or more arguments or elements are expected.

Solution:

const arr1 = [1, 2, 3];

const arr2 = [4, 5, 6];

const combined = [...arr1, ...arr2];

**codidng**
```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const combined = [...arr1, ...arr2];

console.log(combined); 
```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/blob/main/Screenshot%202024-07-05%20070523.png)

**Exercise 7: Rest Parameters**
**Problem Statement:**

Write a function that takes multiple arguments and returns their sum using rest parameters.

Hint/Explanation:

Rest parameters allow us to represent an indefinite number of arguments as an array.

Solution:

const sum = (...numbers) => numbers.reduce((acc, current) => acc + current, 0);

**coding**
```
const sum = (...numbers) => numbers.reduce((acc, current) => acc + current, 0);


console.log(sum(1, 2, 3, 4, 5)); 
console.log(sum(10, 20, 30));    
```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/assets/113282947/d546cc55-2af6-427d-98d7-fad44c0c447b)

**Exercise 8: Default Parameters**
**Problem Statement:**

Create a function greet(name, greeting = "Hello") that greets a person. If no greeting is provided, it should default to "Hello".

Hint/Explanation:

Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.

Solution:

const greet = (name, greeting = "Hello") => ${greeting}, ${name}!;

**coding**
```
const greet = (name, greeting = "Hello") => `${greeting}, ${name}!`;

console.log(greet("Alice"));            
console.log(greet("Alice", "Hi"));      
console.log(greet("Bob", "Good morning")); 
```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/assets/113282947/0f969e73-6e3a-4f45-8eb2-45d38bb66425)

**Exercise 9: Classes and Inheritance**
**Problem Statement:**

Create a class Animal with a constructor setting the name property. Then, create a subclass Dog that extends Animal and adds a bark method.

Hint/Explanation:

ES6 classes are syntactical sugar over JavaScript's existing prototype-based inheritance. The extends keyword is used for class inheritance.

Solution:

class Animal {

constructor(name) {

this.name = name;

}

}

class Dog extends Animal {

bark() {

return Woof! My name is ${this.name};

}

}

**coding**
```
class Animal {
    constructor(name) {
        this.name = name;
    }
}

class Dog extends Animal {
    bark() {
        return `Woof! My name is ${this.name}`;
    }
}

const myDog = new Dog("Buddy");
console.log(myDog.bark());

```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/assets/113282947/df4b2235-4974-4b8a-8734-13b4fb70a180)

**Exercise 10: Promises and Async/Await**
**Problem Statement:**

Create a function waitAndReturn that returns a Promise which resolves with the string "Done" after 2 seconds. Then, use async/await to call this function and log the result.

Hint/Explanation:

Promises are used for asynchronous computations. Async/await is syntactic sugar for working with Promises in a more synchronous fashion.

Solution:

const waitAndReturn = () => new Promise(resolve => setTimeout(() => resolve("Done"), 2000));

async function run() {

const result = await waitAndReturn();

console.log(result);

}

run();

**coding**
```
const waitAndReturn = () => new Promise(resolve => setTimeout(() => resolve("Done"), 2000));

async function run() {
    const result = await waitAndReturn();
    console.log(result);
}

run();

```
**output**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/assets/113282947/a8b84ee9-dc43-4df5-ad0e-ec35d4b63d67)

**Project Assignment: Build a To-Do List Application Using ES6 JavaScript**
Objective:
Create a fully functional To-Do List application using ES6 JavaScript. This project will help you understand and apply ES6 features, such as classes, modules, arrow functions, template literals, and the fetch API.

**coding**

index.html
```
<!DOCTYPE html>
<html>
<head>
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>To-Do List</h1>
    <div class="input-container">
      <input type="text" id="task-title" placeholder="Task Title">
      <textarea id="task-description" placeholder="Description (optional)"></textarea>
      <input type="date" id="task-due-date">
      <button id="add-task-btn">Add Task</button>
    </div>
    <div class="filter-container">
      <label for="filter-status">Filter by Status:</label>
      <select id="filter-status">
        <option value="all">All</option>
        <option value="completed">Completed</option>
        <option value="incomplete">Incomplete</option>
      </select>
    </div>
    <ul id="task-list"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

**style.css**
```
body {
  font-family: sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f4;
}

.container {
  width: 500px;
  margin: 50px auto;
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}

.input-container {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

input[type="text"],
textarea,
input[type="date"] {
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

textarea {
  resize: vertical;
}

button {
  background-color: #4CAF50;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

.filter-container {
  margin-bottom: 20px;
}

#task-list {
  list-style: none;
  padding: 0;
}

#task-list li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  margin-bottom: 10px;
  background-color: #f9f9f9;
  border-radius: 3px;
}

#task-list li.completed {
  text-decoration: line-through;
  color: #888;
}

.actions {
  display: flex;
  gap: 10px;
}

.actions button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  color: #333;
  font-size: 16px;
}
```
**script.js.txt**
```
// script.js
class Task {
  constructor(title, description, dueDate, isCompleted = false) {
    this.title = title;
    this.description = description;
    this.dueDate = dueDate;
    this.isCompleted = isCompleted;
  }
}

class ToDoList {
  constructor() {
    this.tasks = [];
    this.loadTasks();
  }

  addTask(task) {
    this.tasks.push(task);
    this.saveTasks();
    this.renderTasks();
  }

  editTask(index, newTask) {
    this.tasks[index] = newTask;
    this.saveTasks();
    this.renderTasks();
  }

  deleteTask(index) {
    this.tasks.splice(index, 1);
    this.saveTasks();
    this.renderTasks();
  }

  toggleTaskCompletion(index) {
    this.tasks[index].isCompleted = !this.tasks[index].isCompleted;
    this.saveTasks();
    this.renderTasks();
  }

  filterTasks(filterStatus) {
    let filteredTasks = [];
    if (filterStatus === 'all') {
      filteredTasks = this.tasks;
    } else if (filterStatus === 'completed') {
      filteredTasks = this.tasks.filter(task => task.isCompleted);
    } else if (filterStatus === 'incomplete') {
      filteredTasks = this.tasks.filter(task => !task.isCompleted);
    }
    this.renderTasks(filteredTasks);
  }

  saveTasks() {
    localStorage.setItem('tasks', JSON.stringify(this.tasks));
  }

  loadTasks() {
    const storedTasks = localStorage.getItem('tasks');
    if (storedTasks) {
      this.tasks = JSON.parse(storedTasks);
    }
  }

  renderTasks(tasks = this.tasks) {
    const taskList = document.getElementById('task-list');
    taskList.innerHTML = ''; // Clear the list

    tasks.forEach((task, index) => {
      const listItem = document.createElement('li');
      listItem.classList.add('task');
      if (task.isCompleted) {
        listItem.classList.add('completed');
      }

      listItem.innerHTML = `
        <div class="task-content">
          <input type="checkbox" ${task.isCompleted ? 'checked' : ''} data-index="${index}">
          <span>${task.title}</span>
          <span class="due-date">${task.dueDate}</span>
        </div>
        <div class="actions">
          <button class="edit-btn" data-index="${index}">Edit</button>
          <button class="delete-btn" data-index="${index}">Delete</button>
        </div>
      `;

      taskList.appendChild(listItem);
    });

    // Add event listeners for checkboxes, edit, and delete buttons
    const checkboxes = taskList.querySelectorAll('input[type="checkbox"]');
    checkboxes.forEach(checkbox => {
      checkbox.addEventListener('change', () => {
        const index = checkbox.dataset.index;
        toDoList.toggleTaskCompletion(index);
      });
    });

    const editButtons = taskList.querySelectorAll('.edit-btn');
    editButtons.forEach(button => {
      button.addEventListener('click', () => {
        const index = button.dataset.index;
        // Handle edit functionality here
        // You might want to display a modal or update the task directly in the list item
      });
    });

    const deleteButtons = taskList.querySelectorAll('.delete-btn');
    deleteButtons.forEach(button => {
      button.addEventListener('click', () => {
        const index = button.dataset.index;
        toDoList.deleteTask(index);
      });
    });
  }
}

const toDoList = new ToDoList();

const addTaskBtn = document.getElementById('add-task-btn');
addTaskBtn.addEventListener('click', () => {
  const title = document.getElementById('task-title').value;
  const description = document.getElementById('task-description').value;
  const dueDate = document.getElementById('task-due-date').value;

  if (title) {
    const newTask = new Task(title, description, dueDate);
    toDoList.addTask(newTask);
    document.getElementById('task-title').value = '';
    document.getElementById('task-description').value = '';
    document.getElementById('task-due-date').value = '';
  }
});

const filterStatusSelect = document.getElementById('filter-status');
filterStatusSelect.addEventListener('change', () => {
  const filterStatus = filterStatusSelect.value;
  toDoList.filterTasks(filterStatus);
});

// Initial render of tasks
toDoList.renderTasks();
s
```
**output:**
![image](https://github.com/sathiya7g/ES6-Javascript-Assignment/assets/113282947/3f24fde9-1ae8-41d0-8a19-fdfa68165a63)




