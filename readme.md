# Node.js

**1. What is Node.js?**<br>
Node.js is a JavaScript runtime environment that allows us to run JavaScript outside the browser.

**2. Why do we use Node.js?**<br>
There are different reasons for using Node.js:
1. **Backend Development:** To build server-side applications.
2. **API Development:** To create APIs.
3. **Database Connection:** To connect databases such as MongoDB and MySQL.
4. **File Handling:** To create, read, update, and delete files.
5. **Real-time Applications:** To build chat applications and live notifications.
6. **Full-stack Development:** To develop both frontend and backend applications using JavaScript.

**3. Features of Node.js**<br>
- **Asynchronous**	      Handles multiple operations efficiently.
- **Non-blocking**        The entire server does not get blocked while waiting for one operation to complete.
- **Single-threaded**	     Uses a single main thread for JavaScript execution.
- **Fast Execution**	     Built on Google Chrome's V8 JavaScript engine.
- **Event-driven**	         Handles operations through events.
- **Cross-platform**	     Works on Windows, Linux, and macOS.
- **Scalable**	             Can handle multiple client requests efficiently.
- **Open-source**	         Free to use, and its source code is publicly available.


**4. Node.js Architecture**<br>
Node.js architecture explains how Node.js receives requests, executes JavaScript code and handles asynchronous operations.
1. **V8 Engine:** Executes JavaScript code.
2. **Call Stack:** Executes JavaScript functions.
3. **Event Loop:** Helps manage asynchronous operations.
4. **Callback Queue:** Holds ready-to-execute callbacks until they can be processed.
5. **libuv**: Provides asynchronous I/O and event loop functionality.
6. **Thread Pool:** Handles certain background tasks.


----------------------------------------------------------------------------------------------------------------------------------------------------




## 1. Node.js Installation
Node.js installation means downloading and setting up Node.js on our computer so that we can execute JavaScript outside the browser.

**Verify Node.js Installation**
```
node -v                     Example output: v22.15.0
```
**To check the npm version:**
```
npm -v                      Example output: 10.9.2
```
If the versions are displayed, it means both have been successfully installed.

**What is npm?**
npm stands for Node Package Manager. It is used to install and manage packages in Node.js projects.

**Node.js vs NPM**
```
    Node.js         	                 NPM
JavaScript runtime	                Package manager
JS run karta hai	                Packages install karta hai
Backend mein use hota hai	        Dependencies manage karta hai
Server create kar sakte hain	    Libraries install kar sakte hain
```

**Important Commands** <br>

- node -v — Check Node.js version.
- npm -v — Check npm version.
- node index.js — Execute a JavaScript file.
- node — Open Node.js REPL.
- Ctrl + C — Stop a running process or exit REPL.


----------------------------------------------------------------------------------------------------------------------------------------------------


## 2. Node.js REPL and CLI

**What is REPL?**<br>
REPL stands for Read, Evaluate, Print, Loop. It is an interactive environment that allows us to execute JavaScript code directly in the terminal.

**Four Steps of REPL**<br>
- **Read:** Reads the JavaScript code.
- **Evaluate:** Executes the code.
- **Print**: Displays the result.
- **Loop:** Waits for the next command.

**How to Open REPL?**
```
node
```
**How to Exit REPL?**
```
.exit               Or       press Ctrl + C twice.
```

**What is CLI?**
CLI stands for Command Line Interface. It allows users to interact with a computer or software by typing commands in a terminal.

**Important Node.js CLI Commands**

1. **node** — Opens REPL.
2. **node -v** — Checks Node.js version.
3. **npm -v** — Checks npm version.
4. **node index.js** — Executes a JavaScript file.
5. **node --help** — Displays Node.js help.
6. **node --watch index.js** — Automatically restarts the program when files change.


----------------------------------------------------------------------------------------------------------------------------------------------------


## 3. Node.js vs Browser JavaScript










