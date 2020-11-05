# kottans-frontend

## My schedule and progress

- [x] [Git and GitHub](#1-git-and-gitHub)
  - [x] [Git Basics](#11-git-basics)
  - [x] [Git Collaboration](#12-git-collaboration)
- [x] [Linux CLI and HTTP](#2-linux-cli-and-http)
- [x] [HTML & CSS](#3-html--css)
- [x] [JavaScript](#4-javascript)
- [x] [Document Object Model](#5-document-object-model)
  - [x] [Javascript and the Dom](#51-javaScript-and-the-dom)
  - [x] [freecodecamp Algorithm Scripting Challenges](#52-freecodecamp-algorithm-scripting-challenges)

## 1. Git and GitHub

### 1.1. Git Basics

**What learned a new one:**

- [x] What is Version Control?
- [x] Create a Git Repo
- [x] Review a Repo's History
- [x] Add Commits To a Repo
- [x] Tagging, Branching, Merging
- [x] Undoing Changes
- [x] Push & Pull -- Git Remotes
- [x] Git commands: `init`, `clone`, `add`, `commit`, `checkout`, `branch`, `merge`, ...

[![screenshots-placeholder](./screenshots-icon.png)](./git/git-basics)

### 1.2. Git Collaboration

**What learned a new one:**

- [x] Working with remotes
- [x] Working on another developer's repo
- [x] Git commands: `push`, `fetch`, `pull`, ...
- [x] I am better understand pull request and Fork repo
- [x] Staying in Sync With A Remote Repo

[![screenshots-placeholder](./screenshots-icon.png)](./git/git-collaboration)

---

## 2. Linux CLI and HTTP

### 2.1. [Linux Survival](https://linuxsurvival.com/linux-tutorial-introduction/)

- **What learned a new one:**

  - I learned a few new useful commands like `find`, `cat`, `grep` and `echo`.
  - I intend to use such commands: `ls`, `cd`, `touch`, `mkdir`, `pwd`, `chmod`, `grep`, ...
  - `more <file>` to show file content.
  - `mv <any> <dir>` to move file/directory in another directory.
  - `mv <any> <new-name>` to rename file/directory.
  - `cp <file> <dir>`/`cp -r <dir> <dir>` to copy file/directory in another directory.
  - `pwd` to show current directory.
  - `rm <file>`/`rmdir <dir>`/`rm -r <dir>` to remove file/empty directory/non-empty directory.
  - `ls -l` for detailed file listing.
  - `chmod` for managing security permissions on files.
  - `~` as shortcut for current user home directory, `~<user-id>` as shortcut for another user home directory, `.` as a shortcut for current directory, `..` as a shortcut for parent directory.
  - `man <command>`, `man man` for cli commands searching.
  - `cd` with no arg for navigating to current user home directory.
  - `ps`/`pr aux` to show process status/list all processes.
  - `<com-1> | <com-2>` to send output from one command as input to another command (pipe commands). For instance, `ps aux | grep <text>` means:
    1. execute `ps aux` and instead of logging its result in terminal pass it as arg to the next command.
    2. execute `grep <text>` with `<arg>` where arg is the one which received from previous command (if this command wouldn't be part og commands pipe, we should specify arg manually - `grep <text> <arg>`).
  - `grep <text> <file>` to show lines of the containing defined text.
  - `kill <process-id>`, `kill -9 <process-id>` to kill processes.

- **What surprised**

  I was surprised that absolute path starts from `/`. I always used relative paths starting with `./` and used to think that `./` === `/`. By making some experements in terminal i understood that _absolute path_ starts from `/` and _relative path_ starts from `./` or right from file/directory name. I also realized that each command has both input and output where input - set or arguments defined with command and output - content printed in terminal.

- **What will be used in practice**

  I will use most of the commands i acquainted with because it represents 20% of commands which can cover up to 80% of work to do in terminal.

- **General overview**

  I didn't use Linux before, but i have experience with other UNIX-based OS and Windows. Due to fact that Linux is used the most in software engineering, this course was necessary part for me. I was scared a bit at the very beginning but as i started to execute interactive tasks i understood that it is not that big difference between one and another OS (especially between UNIX-based). Thanks to this set of tasks i clarified for myself how paths are constructed. I mean, i always used `cd ../` without knowing of how it actually works. And now i got a context.

[![screenshots-placeholder](./screenshots-icon.png)](./linux-cli/linux-survival.png)

---

## 3. HTML & CSS

- **What learned a new one:**
  - [x] Selectors and Visual Rules
  - [x] The Box Model
  - [x] Display and Positioning
  - [x] Colors & Typography
  - [x] Flexbox
  - [x] Grid

[![screenshots-placeholder](./screenshots-icon.png)](./html-css)

---

## 4. Javascript

- **What learned a new one:**
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

[![screenshots-placeholder](./screenshots-icon.png)](./js/FFC_JavaScript_Algorithms_and_Data_Structures_Certification.png)

---

## 5. Document Object Model

### 5.1. [JavaScript and the DOM](https://classroom.udacity.com/courses/ud117)

- **What learned a new one:**
  - The `.appendChild()` method will move an element from its current position to the new position.
  - I learned difference between `textContent` and `innerText` properties:
    - `textContent` prop returns original version of content, while `innerText` - rendered one (considers css styles).
    - `textContent` gets the content of all elements, including `<script>` and `<style>` elements while `innerText` only shows content of “human-readable” elements.
  - The Chrome browser has a special `monitorEvents()` function that will let us see different events as they are occurring.
  - I learned about event handling strategies:
    - _from inner to outer_ (default) - invoke events from target to outermost. Listeners invoked in bubbling stage.
    - _from outer to inner (with 3rd arg true)_ - invoke events from outermost to target. Listeners invoked in capturing stage.
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

- **What surprised**

  - Info that due to support issues earlier developers had to write different code to perform the same action in different browsers. Handling this was one of the main purposes of jQuery. You write abstract, jQuery-specific methods, jQuery converts it to compatible for different browser methods. Now browsers try to support standarts so jQuery is not that used. I was surprised to know that jQuery triggered development of new DOM methods.
  - Info that event callbacks are called _listeners_(listener function) and defining callback called _listener registration_.
  - Ability to see/temporary remove registered event of selected element and its ancestors in `Event` tab.
  - I learned how to replace 1 big block of code which executed synchronously with n small blocks of code which executed asynchronously (by using `SetTimeout` with zero delay). Why it is important? Because when sync block of code too big, it will occupy the stack for too long and it will be noticeable for user. For example, when `for loop` starts to run, all other commands won't be able to run on stack and if cycle runs long time page inaccessibility will be noticeable. If the cycle runs for 5 seconds, the user won't be able to interact with the page in any way for 5 seconds.

- **What will be used in practice**
  - Break Up Long-Running Code
  - Methods to select/modify/delete DOM elements.
  - Event objects, event phases, event delegation and Events tab in devtools.
  - Code performance testing and optimization.

[![screenshots-placeholder](./screenshots-icon.png)](./document-object-model/JavaScript-and-the-DOM.png)

### 5.2. [freecodecamp Algorithm Scripting Challenges](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/)

[![screenshots-placeholder](./screenshots-icon.png)](./document-object-model/freecodecamp-Algorithm-Scripting-Challenges.png)

---
