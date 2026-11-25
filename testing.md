
# Node.js Complete Notes

## Table of Contents

1. [Node.js Introduction](#1-nodejs-introduction)
2. [Node.js Installation](#2-nodejs-installation)
3. [Node.js REPL and CLI](#3-nodejs-repl-and-cli)
4. [Node.js vs Browser JavaScript](#4-nodejs-vs-browser-javascript)
5. [Modules: Built-in, Core, Custom and Third-party](#5-modules-built-in-core-custom-and-third-party)
6. [CommonJS Modules and ES Modules](#6-commonjs-modules-and-es-modules)
7. [require(), module.exports, exports, import and export](#7-require-moduleexports-exports-import-and-export)
8. [Named Exports and Default Exports](#8-named-exports-and-default-exports)
9. [Important Node.js Built-in Modules](#9-important-nodejs-built-in-modules)

---

# 1. Node.js Introduction

## 1.1 What is Node.js?

Node.js is a JavaScript runtime environment that allows us to run JavaScript outside the browser.

## 1.2 Why do we use Node.js?

There are different reasons for using Node.js:

1. **Backend Development:** To build server-side applications.
2. **API Development:** To create APIs.
3. **Database Connection:** To connect databases such as MongoDB and MySQL.
4. **File Handling:** To create, read, update, and delete files.
5. **Real-time Applications:** To build chat applications and live notifications.
6. **Full-stack Development:** To develop both frontend and backend applications using JavaScript.

## 1.3 Features of Node.js

- **Asynchronous:** Handles multiple operations efficiently.
- **Non-blocking:** The entire server does not get blocked while waiting for one operation to complete.
- **Single-threaded:** Uses a single main thread for JavaScript execution.
- **Fast Execution:** Built on Google Chrome's V8 JavaScript engine.
- **Event-driven:** Handles operations through events.
- **Cross-platform:** Works on Windows, Linux, and macOS.
- **Scalable:** Can handle multiple client requests efficiently.
- **Open-source:** Free to use, and its source code is publicly available.

## 1.4 Node.js Architecture

Node.js architecture explains how Node.js receives requests, executes JavaScript code and handles asynchronous operations.

1. **V8 Engine:** Executes JavaScript code.
2. **Call Stack:** Executes JavaScript functions.
3. **Event Loop:** Helps manage asynchronous operations.
4. **Callback Queue:** Holds ready-to-execute callbacks until they can be processed.
5. **libuv:** Provides asynchronous I/O and event loop functionality.
6. **Thread Pool:** Handles certain background tasks.

---

# 2. Node.js Installation

Node.js installation means downloading and setting up Node.js on our computer so that we can execute JavaScript outside the browser.

## 2.1 Verify Node.js Installation

```bash
node -v
```

Example output: `v22.15.0`

```bash
npm -v
```

Example output: `10.9.2`

If the versions are displayed, it means both have been successfully installed.

## 2.2 What is npm?

npm stands for Node Package Manager. It is used to install and manage packages in Node.js projects.

## 2.3 Node.js vs NPM

| Node.js | NPM |
|---|---|
| JavaScript runtime | Package manager |
| JS run karta hai | Packages install karta hai |
| Backend mein use hota hai | Dependencies manage karta hai |
| Server create kar sakte hain | Libraries install kar sakte hain |

## 2.4 Important Commands

- `node -v` — Check Node.js version.
- `npm -v` — Check npm version.
- `node index.js` — Execute a JavaScript file.
- `node` — Open Node.js REPL.
- `Ctrl + C` — Stop a running process or exit REPL.

---

# 3. Node.js REPL and CLI

## 3.1 What is REPL?

REPL stands for Read, Evaluate, Print, Loop. It is an interactive environment that allows us to execute JavaScript code directly in the terminal.

## 3.2 Four Steps of REPL

- **Read:** Reads the JavaScript code.
- **Evaluate:** Executes the code.
- **Print:** Displays the result.
- **Loop:** Waits for the next command.

## 3.3 How to Open REPL?

```bash
node
```

## 3.4 How to Exit REPL?

```bash
.exit
```

Or press `Ctrl + C` twice.

## 3.5 What is CLI?

CLI stands for Command Line Interface. It allows users to interact with a computer or software by typing commands in a terminal.

## 3.6 Important Node.js CLI Commands

1. **node** — Opens REPL.
2. **node -v** — Checks Node.js version.
3. **npm -v** — Checks npm version.
4. **node index.js** — Executes a JavaScript file.
5. **node --help** — Displays Node.js help.
6. **node --watch index.js** — Automatically restarts the program when files change.

---

# 4. Node.js vs Browser JavaScript

## 4.1 What is Browser JavaScript?

Browser JavaScript is JavaScript that runs inside a web browser, such as Google Chrome, Firefox, or Microsoft Edge.

### Browser JavaScript Global Objects

| Global Objects | Purpose |
|---|---|
| window | Represents the browser window. |
| document | Provides access to the HTML document (webpage). |

### Example:

```js
// in browser

console.log(window);    // → Works
console.log(document);  // → Works

// in node.js

console.log(global);    // → Not available by default (ReferenceError)
console.log(process);   // → Not available by default (ReferenceError)
```

## 4.2 What is Node.js?

Node.js is a JavaScript runtime environment that allows us to run JavaScript outside the browser.

### Node.js ke Global Objects

| Global Objects | Purpose |
|---|---|
| global | Represents the global object in Node.js. |
| process | Provides information about and the current Node.js process. |

### Example:

```js
// in browser

console.log(window);    // → Not available (ReferenceError)
console.log(document);  // → Not available (ReferenceError)

// in node.js

console.log(global);    // → Works
console.log(process);   // → Works
```

`globalThis` -> Modern JavaScript mein globalThis bhi hota hai, jo browser aur Node.js dono mein global object ko access karne ka standard tareeqa hai.

```js
// in browser

console.log(globalThis);   // -> return Window object

// in node.js

console.log(globalThis);   // -> return global object
```

### IN BROWSER

```js
console.log(globalThis.window);

console.log(globalThis.document);
```

### IN NODE.JS

```js
console.log(globalThis.global);

console.log(globalThis.process);
```

---

# 5. Modules: Built-in, Core, Custom and Third-party

Module is a reusable piece of code that we can use in different files of our project.

## 5.1 Types of Node.js Modules

- **Built-in:** Already provided by Node.js.
- **Custom:** Created by developers.
- **Third-party:** Installed separately.

### 5.1.1 Built-in Modules

Built-in modules are modules that come pre-installed with Node.js.

| Module | Purpose |
|---|---|
| `fs` | Files handle karna |
| `path` | File paths manage karna |
| `http` | HTTP server create karna |
| `os` | Operating system information |
| `events` | Events handle karna |
| `crypto` | Encryption aur hashing |
| `url` | URLs handle karna |
| `stream` | Data ko chunks mein handle karna |
| `buffer` | Binary data handle karna |

### 5.1.2 Custom Modules

Custom modules are modules that developers create themselves according to their project requirements.

```text
myProject/

│
├── index.js
└── math.js
```

### 5.1.3 Third-party Modules

Third-party modules are packages created by other developers and installed separately to use in our projects.

| Package | Purpose |
|---|---|
| Express | Backend server aur routing |
| Mongoose | MongoDB ke saath work karna |
| dotenv | Environment variables manage karna |
| cors | Cross-origin requests control karna |
| bcrypt | Password hashing |
| nodemon | Development mein server restart karna |

When we install a third-party package, npm creates a `node_modules` folder inside the project.

- **node_modules** → Installed packages aur unki dependencies contain karta hai.
- **package.json** → Project information aur dependencies contain karta hai.
- **package-lock.json** → Installed dependencies ki exact versions aur dependency tree record karta hai.

---

# 6. CommonJS Modules and ES Modules

## Example

Suppose you are creating a project. In that project:

- `app.js` — Main file
- `math.js` — Mathematical functions
- `user.js` — User-related functions

### Importing and Exporting Modules

| Operation | CommonJS | ES Modules |
|---|---|---|
| Import a module | `require()` | `import` |
| Export a module | `module.exports` | `export` |

### In package.json File

1. `"type": "module"` → ES Modules (import/export) use kar sakte hain.
2. `"type": "commonjs"` → CommonJS (require/module.exports) use kar sakte hain.

---

# 7. require(), module.exports, exports, import and export

## What is module.exports?

module.exports is used to export code from a CommonJS module so that other files can use it.

### math.js file

```js
function add(a, b) {

    return a + b;

}

module.exports = add;
```

## What is require()?

require() is used to import code from another file or module in CommonJS.

### app.js file

```js
const add = require("./math");

console.log(add(10, 20));
```

---

# 8. Named Exports and Default Exports

### math.js file

```js
// DEFAULT-EXPORT

function add(a, b) {

    return a + b

}

module.exports = add;

// NAME-EXPORT

function add2(a, b) {

    return a + b

}

let myname = "atruba";

module.exports = { add2, myname };
```

### index.js file

```js
// DEFAULT-EXPORT

const add = require("./math.js");

console.log(add(10,20));

// NAME-EXPORT

const { myname, add2 } = require("./math");

console.log(add2(10,10));

console.log(myname);
```

---

# 9. Important Node.js Built-in Modules

## 9.1 FS Module (File System)

The fs module allows us to create, read, update and delete files and directories.
