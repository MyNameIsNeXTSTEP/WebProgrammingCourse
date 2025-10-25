**Task 1: Component-Based Thinking**
- Create an HTML structure:
```html
<div id="app">
  <div id="user-form">
    <input type="text" id="nameInput" placeholder="Name">
    <input type="email" id="emailInput" placeholder="Email">
    <button id="addUser">Add User</button>
  </div>
  <div id="users-container"></div>
</div>
```

- Implement the component function:
```JavaScript
 /**
  * Create a card element with HTML as:
  * `
    <h2>${user.name}</h2>
    <p>${user.email}</p>
    <button class="delete-btn">Delete</button>
    <button class="edit-btn">Edit</button>
  `
  *
  * Use function declaration!
  */

 /**
  * Add event listeners on card for:
  * 1. Deletion
  * 2. Adding
  * 3. Update
  * 
  * Use arrow function expression!
  */
```

Student Tasks:
- Add edit functionality to the user card
- Implement form validation
- Add card styling with CSS
- Create a search/filter function for cards
- Implement local storage as the `Map` to persist the data

---

**Task 2: Custom State Manager Practice**

- Basic structure setup:
```JavaScript
class TodoManager {
  constructor(rootElement) {
    this.root = rootElement;
    this.todos = [];
    this.filterState = 'all'; // all, active, completed
    
    this.init();
  }

  init() {
    this.createUI();
    this.addEventListeners();
    this.render();
  }
};
```

Student Tasks:
- Implement CRUD operations for todos
- Add filtering (all/active/completed)
- Create a counter for remaining tasks
- Add priority levels to todos
- Implement drag-and-drop reordering
- Add due dates to todos

---

**Task 3: Development Setup using NPM package manager and GIT**
Project structure to be implemented:

```txt
project/
├── src/
│   ├── index.html
│   ├── styles/
│   │   └── main.css
│   ├── components/
│   └── assets/
├── package.json
└── .gitignore
```

Student Tasks:
- Set up a development GIT based repository to track changes
	- [Configure](https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github#initializing-a-git-repository) your GIT repository
	- Push your project and the branches to origin *(meaning remote)* repository to your personal GitHub acc
	- Start a side branch from the original one using command: ``
	- Use then `npm` *(command: `npm init`)* to [start an application project](https://weaintplastic.github.io/web-development-field-guide/Development/Frontend_Development/Setting_up_your_project/Setup_Dependency_Managers/Node_Package_Manager/Initialize_NPM_on_a_new_project.html)
- Using GIT - stage first changes you're ok with and commit them in the side branch
- Create scripts for development and production *(`package.json` field "scripts")*
- Describe in details *(may use EN or RUS language)* each step you have done to develop this project, meaning:
	- GIT commands, their order and reasons
	- NPM scripts and their reasons, how to work with them
- Get the link of the branch on the remote repository and provide it to your mentor