# JavaScript

A personal repository for JavaScript projects and learning. This repo contains various JavaScript exercises, experiments, and projects to practice and improve my web development skills.

## Getting Started

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/JayJainTech/JavaScript.git
cd JavaScript
npm install
```

The `node_modules` folder is not included in the repository (see `.gitignore`). Running `npm install` will recreate it based on `package-lock.json`.

### npm run dev

For development with **auto-reload on file changes**:

```bash
npm run dev
```

This uses **nodemon** to automatically restart your Node.js script whenever you save changes. Perfect for iterative development in the WebStorm console.

**Note on `prompt()`**: The `prompt()` function is built-in for browsers but doesn't exist in Node.js. This project uses [prompt-sync](https://www.npmjs.com/package/prompt-sync) to provide browser-like prompt functionality in Node.js. 

To use `prompt()` in your scripts, add this line at the top:

```javascript
require('./.utils.js');
```

This loads `.utils.js` which sets up `prompt()` globally. Then you can use it like in a browser to get user input:

```javascript
let name = prompt("What is your name?");
console.log("Hello, " + name);
```

Great for interactive scripts and getting user input without external dependencies!

### npm run browser

For browser testing with **auto-reload on file changes**:

```bash
npm run browser
```

This launches **live-server** on port 8000 with automatic browser refresh whenever you save changes. Perfect for testing JavaScript in the browser.