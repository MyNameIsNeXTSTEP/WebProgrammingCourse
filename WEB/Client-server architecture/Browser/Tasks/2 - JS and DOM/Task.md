## JavaScript Fundamentals

**Variables and Data Types**

```JavaScript
// Task 1: Create and manipulate different data types
let numberExample = 42;
let stringExample = 'Hello World';
let objectExample = { name: 'John', age: 25 };

// Your task: Create an array of objects representing students
// Each object should have: name, grade, and isActive properties
```

**Array Methods**

```JavaScript
// Task 2: Practice array manipulation
const numbers = [1, 2, 3, 4, 5];
numbers.map(num => num * 2);

// Your task: Create a function that filters out all negative numbers
// and doubles the positive ones
```

## DOM Manipulation

**Element Creation**

```JavaScript
// Task 3: Create a dynamic list
function createList() {
  const ul = document.createElement('ul');
  const items = ['Item 1', 'Item 2', 'Item 3'];
  items.forEach(item => {
    const li = document.createElement('li');
    li.textContent = item; ul.appendChild(li);
  });
  document.body.appendChild(ul);
};
// Your task: Modify this function to add delete buttons for each item
```

**Event Handling**

```JavaScript
// Task 4: Create an interactive form
const form = document.createElement('form');
const input = document.createElement('input');
input.addEventListener('input', (e) => {
  console.log(e.target.value);
});
// Your task: Add validation that checks if input is empty
```

## Chrome DevTools Tasks

**Console Debugging**

```JavaScript
// Task 5: Debug this function
function calculateTotal(prices) {
  let total = 0;
  prices.forEach(price => {
    total += price;
  });
  return total;
};
// Add console.log statements to track the total variable
```

**Breakpoint Practice**

```JavaScript
// Task 6: Add bugs to this code and fix them using DevTools
function findUser(users, id) {
  const user = users.find(u => u.id === id);
  return user.name.toUpperCase();
};

// Your task: Add error handling and use DevTools to debug
// Take screenshots or video of the process
```

## Practice Questions

1. Create a function that adds a class 'highlight' to elements when clicked
2. Implement a simple todo list with add/remove functionality
3. Create a form validation that checks:
    
    - Email format
    - Password strength
    - Matching password confirmation
    

## Final Project

Create a dynamic table with the following features:

Requirements:
1. Add new rows dynamically
2. Sort columns by clicking headers
3. Filter data using an input field
4. Delete rows with a confirmation dialog`

**Debugging Tasks**

- Use `console.table()` to display your data structure
- Add debugger statements in key functions
- Practice using network tab to monitor API calls
- Use performance tab to optimize your code
