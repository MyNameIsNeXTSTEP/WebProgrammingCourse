## **HTML DOM (Document Object Model)**

### Prerequesities

1. You need a [GIT](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) loacally installed
   
2. Create a remote GitHub repository for the course tasks, name it:
   **"WebProgrammingCourse-tasks"**:
   - [Create GitHub repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories#create-a-repository)
   - [Clonning a remote repository locally](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
   - After clonning (in the terminal):
     - Go to the cloned repository locally in the termial with this command:
       `cd WebProgrammingCourse-tasks`
    
     - Then, checkout a new working branch with this command:
       `git checkout -b name_of_your_branch`
    
     - Now you can start working in a side working branch, and after push your changes to the settled remote branch connected to your local one.

3.  Create inside - a task folder for this topic and name it: **"web"**.
   And then do the following.
   Create inside the `web` directory the `browser` folder and inner `HTML DOM` folder for the first task.
   
   So your whole structure would look like this:
```
/WebProgrammingCourse-tasks
|-- /web
    |-- /browser
        |-- /HTML DOM
```

You need to create there some files for the base WEB working page including HTML, CSS, JS:
- index.html
- style.css
- script.js

> Note that the names (index, styles, script) are just conventional, so they might be named in another way tihout any issue, it's just common to name them like that.

---

For you to start without any problem at the beginning let's get this files from my sample -> [here](/WEB/Client-server%20architecture/Browser/1%20-%20HTML%20DOM/sample)
Copy those three files inside your `/web/browser/HTML DOM` folder.

<u>Now you can push your first initial project changes to the GitHub</u>:
- Check the existing status of youe project *(see changed fiels and folders)* with this command:
  `git status`

- Add changed (new) files to the <u>git stage</u> *(a place of git mechanism to be ready to do some operation on changed files and folders)* with this command:
  `git add .`
  *the `.` dot symbols means "everything"*

- Commit your chnages with a special message by this command:
  `git commit -m '[WEB] Browser topic: first task - HTML DOM'`

- If everything was done correctly you'll see the message of changes being commited

- The last thing is to push the commit to the remote branch *(also creating it at first)* by this command:
  `git push --set-upstream origin name_of_your_local_branch`
  *This command does the following: `--set-upstream` creates a remote branch by a provided name and connects it to your local branch; `origin` means to work with remote repository*

---
### Theoretical Tasks:

1. Define the Document Object Model (DOM) and explain how it represents an HTML document.
2. List and describe the primary node types in the DOM, including their roles in the HTML structure.
3. Explain how the DOM differs from the original HTML structure of a page.

> Create a text file in your `/web/browser/HTML DOM` folder with answers to these question above
### Practical Tasks:

1. Write JavaScript code *(at script.js file)* to:
    - Access an element with a specific ID (only one element in the current HTML DOM has an ID, so find it) and change its text content
    - Add a new child element to this selected node as `<a>` tag element with some hyperlink in it.
    - Remove an h1 element from the DOM
3. * Set up an event on clicking a button that changes the background color of the whole page. Use DOM manipulation to achieve this.
   *(also code at script.js file)*

> After solving all tasks - go again over the steps to <u>commit</u> and <u>push</u> the changes to your remote branch.
> 
> !!! But for now !!!
> Since you have already set a remote branch by `--set-upstream origin` command, now you only need after commiting to just push with this simple command:
> `git push`