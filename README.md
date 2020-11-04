# Kottans Git Course

## My schedule and progress

- [x] [Git and GitHub](#git)
  - [Git Basics](#git-basics)
  - [Git Collaboration](#git-collaboration)
- [x] [Linux CLI and HTTP](#linux-cli-and-http)
- [x] [HTML & CSS](#html--css)
- [x] [JavaScript](#javascript)

## Git

### _Git Basics_

**What learned a new one:**

- [x] What is Version Control?
- [x] Create a Git Repo
- [x] Review a Repo's History
- [x] Add Commits To a Repo
- [x] Tagging, Branching, Merging
- [x] Undoing Changes
- [x] Push & Pull -- Git Remotes
- [x] Git commands: `init`, `clone`, `add`, `commit`, `checkout`, `branch`, `merge`, ...

[![screenshots-icon](./screenshots-icon.png)](./git/git-basics)

### _Git Collaboration_

**What learned a new one:**

- [x] Working with remotes
- [x] Working on another developer's repo
- [x] Git commands: `push`, `fetch`, `pull`, ...
- [x] I am better understand pull request and Fork repo
- [x] Staying in Sync With A Remote Repo

[![screenshots-icon](./screenshots-icon.png)](./git/git-collaboration)

---

## Linux CLI and HTTP

_It is very unusual to work from the command line._

**What learned a new one:**

- [x] I learned a few new useful commands like `find`, `cat`, `grep` and `echo`.
- [x] I intend to use such commands: `ls`, `cd`, `touch`, `mkdir`, `pwd`, `chmod`, `grep`, ...
- [x] navigation across file system
- [x] manipulating files
- [x] security, permissions, users and groups, user info
- [x] important locations in the file system
- [x] built-in help
- [x] output redirection and piping
- [x] printing
- [x] wild cards and patterns
- [x] finding files and text
- [x] processes

[![screenshots-icon](./screenshots-icon.png)](./linux-cli/linux-survival.png)

---

## HTML & CSS

**What learned a new one:**

- [x] Selectors and Visual Rules
- [x] The Box Model
- [x] Display and Positioning
- [x] Colors & Typography
- [x] Flexbox
- [x] Grid

[![screenshots-icon](./screenshots-icon.png)](./html-css)

---

## Javascript

**What learned a new one:**

- [x] Basic javascript
- [x] ES6
- [x] Regular expression
- [ ] Debugging
- [x] Basic data structures
- [x] Basic algorithm scripting
- [x] Object oriented programming
- [x] Functional programming
- [x] Intermediate algorithm scripting
- [ ] JavaScript algorithms and data structures projects

[![screenshots-icon](./screenshots-icon.png)](./js/FFC_JavaScript_Algorithms_and_Data_Structures_Certification.png)

---

## Document Object Model

- JavaScript and the DOM

  - **What learned a new one:**
    - The `.appendChild()` method will move an element from its current position to the new position.
    - The Chrome browser has a special `monitorEvents()` function that will let us see different events as they are occurring.
    - The standard way to measure how long it takes code to run is by using `performance.now()`.
    - Changes made to a DocumentFragment `.createDocumentFragment()` happen off-screen; there's no reflow and repaint cost while you build this.
  - **What surprised**

    - Break Up Long-Running Code

      ```javascript
      let count = 1;

      function generateParagraphs() {
        const fragment = document.createDocumentFragment();

        for (let i = 1; i <= 500; i++) {
          const newElement = document.createElement("p");
          newElement.textContent = "This is paragraph number " + count;
          count = count + 1;

          fragment.appendChild(newElement);
        }

        document.body.appendChild(fragment);

        if (count < 20000) {
          setTimeout(generateParagraphs, 0);
        }
      }

      generateParagraphs();
      ```

  - **What will be used in practice**
    - Break Up Long-Running Code

  [![screenshots-icon](./screenshots-icon.png)](./document-object-model/JavaScript-and-the-DOM.png)

- freecodecamp Algorithm Scripting Challenges
  - **What learned a new one:** text placeholder
  - **What surprised** text placeholder
  - **What will be used in practice** text placeholder
  - **General overview** text placeholder

---
