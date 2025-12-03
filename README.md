# ISIT 300 Web Technologies Course Review
We have covered a lot of topcis in this course, it would be easy to forget all of the details. This document is a review of concepts and topics covered in the course.

## HTML
A tagged markup up language used to describe the document structure. This course covered the basics of what HTML is capable of and there is plenty more to explore. To keep learning more about HTML the MDN docs are an excellent source for seeing what is available. 

### Formatting Tags
* `<strong>` - Bold text
* `<em>` - Italic text
* `<sup>` - Superscript text
* `<sub>` - Subscript text
* `<code>` - Code text
* `<pre>` - Pre-formatted text
* `<blockquote>` - Blockquote text
* `<q>` - Short inline quotation

### Sections and Layout tags
* `<header>` - Header section
* `<footer>` - Footer section
* `<article>` - Article section
* `<section>` - Section section
* `<nav>` - Navigation section
* `<aside>` - Aside section
* `<main>` - Main section
* `<figure>` - Figure section
* `<figcaption>` - Figure caption
* `<details>` - Details section
* `<summary>` - Summary section

### Forms
Forms allow users to input and submit data to a web application. They are essential for user interaction on websites.

* `<form>` - Container element that wraps form inputs and defines where data should be sent
* `<input>` - Creates various input fields (text, email, password, checkbox, radio, etc.)
* `<select>` - Creates a dropdown menu for selecting from multiple options

**Example:**
```html
<form action="/submit" method="POST">
  <input type="text" name="username" placeholder="Enter username">
  <input type="email" name="email" placeholder="Enter email">
  <select name="country">
    <option value="us">United States</option>
    <option value="ca">Canada</option>
  </select>
  <button type="submit">Submit</button>
</form>
```

### CSS and JS
* `<style>` - Sets up a style block
* `<script>` - sets up a script block

### The DOM 
DOM stands for document object model. It holds the node tree for the document. When adding HTML tags or using Javascript to make changes you work with the DOM and its apis. 

## CSS
We lightly touched on CSS in this course. However, there are some important concepts to remember. If you would like to continue to learning more about CSS. the MDN docs are an excellent place to look up properties and try something out.

### Selectors
* Type selector - Selects all elements of the given type
* Class selector - Selects all elements with the given class
* ID selector - Selects all elements with the given ID
* Attribute selector - Selects all elements with the given attribute
* Pseudo-class selector - Selects all elements that match the pseudo-class
* Pseudo-element selector - Selects a part of the selected element

### Properties
CSS properties control the visual appearance and layout of HTML elements.

* **Color** - Sets the text color (e.g., `color: blue;` or `color: #FF0000;`)
* **Background color** - Sets the background color of an element (e.g., `background-color: yellow;`)
* **Font** - Controls text appearance including family, size, weight (e.g., `font-family: Arial; font-size: 16px;`)
* **Display** - Controls how elements are displayed (`block`, `inline`, `flex`, `grid`, `none`)
* **Position** - Controls element positioning (`static`, `relative`, `absolute`, `fixed`, `sticky`)
* **Padding** - Space inside an element, between content and border (e.g., `padding: 10px;`)
* **Margin** - Space outside an element, between elements (e.g., `margin: 20px;`)

**Example:**
```css
.my-box {
  color: #333;
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
  font-size: 16px;
  display: block;
  position: relative;
  padding: 15px;
  margin: 10px;
}
```

## Linking Documents
External documents can be linked within HTML. This allows you to break apart your work into multiple files that can be reused or managed differently for performance needs.

**Common linking methods:**

* **CSS Files** - Link external stylesheets in the `<head>` section:
```html
<link rel="stylesheet" href="styles.css">
```

* **JavaScript Files** - Link external scripts, typically before closing `</body>`:
```html
<script src="script.js"></script>
```

* **Images** - Reference images from external sources:
```html
<img src="image.jpg" alt="Description">
```

* **Hyperlinks** - Link to other pages or external resources:
```html
<a href="page.html">Link Text</a>
<a href="https://example.com">External Link</a>
```

## Version Control
While not strictly a web technology git's influence cannot be understated when it comes to the web. Anytime you work on something it is useful to add a repository, working with teams and CI/CD structures it is vital. 

### Git

Git is a distributed version control system designed to help users track changes in their code, collaborate with others, and manage different versions of a project over time. It's essential for teamwork, backup, and understanding the history of your codebase.

#### What is GitHub?
GitHub is a web platform for hosting git repositories. It provides a graphical interface to your code, tools for sharing, reviewing, opening issues, managing pull requests, and collaborating with anyone worldwide.

#### Initializing a Repository
Create a new git repository in your project folder:
```bash
git init
```

#### Cloning a Repository
Download a remote repository (such as from GitHub):
```bash
git clone https://github.com/username/repository.git
```

#### Checking Status
Display modified, added, or deleted files:
```bash
git status
```

#### Adding Files
Stage file(s) for commit:
```bash
git add filename.txt # Add a single file
git add .            # Add all files & folders
```

#### Commiting
Save a snapshot of staged changes:
```bash
git commit -m "Your commit message here"
```

#### Branching
Create and switch between branches to safely develop features:
```bash
git branch feature-xyz       # Create a new branch
git checkout feature-xyz     # Switch to branch
git checkout -b new-feature  # Create and switch in one step
```

#### Remotes
Git remotes point to versions of your repository on GitHub or elsewhere.
```bash
git remote add origin https://github.com/yourname/repo.git
```

#### Push / Pull / Fetch
To share/pull code with/from a remote:
```bash
git push origin main       # Upload your changes to main branch
git pull origin main       # Get latest updates from main branch
git fetch                 # Fetch changes (doesn’t merge)
```

#### Log and History
See commit history:
```bash
git log
```

#### Merge & Resolve Conflicts
To combine branches, use:
```bash
git merge branchname
```
If you see a merge conflict, open the files and edit as needed, then:
```bash
git add conflict-file.js
git commit
```

### Github
GitHub hosts git repositories in the cloud and provides tools for: code review, issue tracking, and teamwork. Create an account, push your repo, and collaborate with the world—all using git and the above commands.

## Javascript
Javascript is a vast subject and in many way a primary character in the world of development / engineering. There is far more to learn than could be covered in a single class.

#### IF / ELSE statements
Used to make decisions in code based on conditions. The code executes different blocks depending on whether a condition is true or false.

**Example:**
```javascript
let age = 18;

if (age >= 18) {
  console.log("You are an adult");
} else {
  console.log("You are a minor");
}

// Multiple conditions
if (score >= 90) {
  grade = "A";
} else if (score >= 80) {
  grade = "B";
} else {
  grade = "C";
}
```

### For Each
A method that loops through each element in an array or object, executing a function for each item. This is cleaner than traditional for loops when you need to process every element.

**Example:**
```javascript
const fruits = ["apple", "banana", "orange"];

fruits.forEach(function(fruit) {
  console.log(fruit);
});

// Using arrow function (modern syntax)
fruits.forEach(fruit => console.log(fruit));

// With index
fruits.forEach((fruit, index) => {
  console.log(`${index}: ${fruit}`);
});
``` 

### Function
The keyword for creating a new function. Remember that functions are variables and can be stored as properties, added to classes, or generated by other functions. Functions allow you to reuse code and organize your program into logical blocks.

**Example:**
```javascript
// Function declaration
function greet(name) {
  return "Hello, " + name;
}

// Function expression (stored in a variable)
const add = function(a, b) {
  return a + b;
};

// Arrow function (modern syntax)
const multiply = (a, b) => a * b;

// Function as a property
const calculator = {
  add: function(a, b) { return a + b; },
  subtract: (a, b) => a - b
};
```

### Callbacks
A callback is a concept where a function accepts another function or reference to a function. This is a common pattern in event-based systems. The callback function is executed later, often after an event occurs or an asynchronous operation completes.

**Example:**
```javascript
// Simple callback
function processData(data, callback) {
  const result = data * 2;
  callback(result);
}

processData(5, function(result) {
  console.log("Result:", result); // Output: Result: 10
});

// Common in event listeners
button.addEventListener('click', function() {
  console.log('Button clicked!');
});

// Array methods use callbacks
const numbers = [1, 2, 3, 4];
numbers.forEach(function(num) {
  console.log(num * 2);
});
``` 

### Variable Scope
Variable scope determines where a variable can be accessed in your code. Understanding scope helps prevent bugs and organize your code properly.

#### Const
Creates a constant variable that cannot be reassigned after declaration. Use `const` for values that shouldn't change. Note: For objects and arrays, the contents can still be modified, but you can't reassign the variable itself.

**Example:**
```javascript
const pi = 3.14159;
// pi = 3.14; // Error: cannot reassign

const person = { name: "John" };
person.name = "Jane"; // OK - modifying object property
// person = {}; // Error - cannot reassign
```

#### Let
Creates a block-scoped variable that can be reassigned. Use `let` when you need a variable that might change value, and you want it scoped to the nearest block (curly braces).

**Example:**
```javascript
let count = 0;
count = 5; // OK - can reassign

if (true) {
  let message = "Inside block";
  console.log(message); // Works
}
// console.log(message); // Error - message not accessible outside block
```

#### Closures
A closure occurs when an inner function has access to variables from its outer (enclosing) function, even after the outer function has finished executing. This allows functions to "remember" their environment.

**Example:**
```javascript
function createCounter() {
  let count = 0; // Private variable
  
  return function() {
    count++; // Inner function accesses outer variable
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
// count is not accessible from outside, but the inner function remembers it
```

#### Block Scope
Variables declared with `let` and `const` are block-scoped, meaning they only exist within the block (curly braces `{}`) where they're declared. This prevents variable conflicts and makes code more predictable.

**Example:**
```javascript
if (true) {
  let x = 10;
  const y = 20;
  console.log(x, y); // Works: 10, 20
}
// console.log(x, y); // Error: x and y not accessible here

// Each block has its own scope
for (let i = 0; i < 3; i++) {
  console.log(i); // 0, 1, 2
}
// console.log(i); // Error: i not accessible outside loop
```

## ASYNC / AWAIT
A combination of keywords that allow you to run code outside of the typical line-by-line manner. This is essential for operations that take time (like fetching data from a server) without freezing the browser. 

### ASYNC
used before the function keyword, flags a function to run asycronously. Async functions expect to return promises.

### AWAIT
Used before function calls. This keyword instructs the browser to stop and await the result of an asyncronous function 

### Promise
An object containing information about the state of an asynchronous function. A Promise represents a value that may be available now, in the future, or never. It has three states: pending, fulfilled (success), or rejected (error).

**Example:**
```javascript
const myPromise = new Promise((resolve, reject) => {
  // Simulate async operation
  setTimeout(() => {
    const success = true;
    if (success) {
      resolve("Operation completed!");
    } else {
      reject("Operation failed!");
    }
  }, 1000);
});

myPromise
  .then(result => console.log(result))
  .catch(error => console.error(error));
``` 

### Fetch
An API that allows you to pull information from external sources (like web servers) and return results to your script. It's the modern way to make HTTP requests in JavaScript.

**Example:**
```javascript
// Basic fetch
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));

// Using async/await
async function getData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
}
```

### Event Listeners
The browser and Javascript together supply numerous events that can be listened (subscribed) to. Using event listeners allows you to respond to events like clicks, key presses, scrolling, and many more to create functionality. 

#### Click Event
Fires when a user clicks on an element. One of the most common events for interactive web pages.

**Example:**
```javascript
const button = document.querySelector('button');

button.addEventListener('click', function() {
  console.log('Button was clicked!');
  alert('Hello!');
});

// Using arrow function
button.addEventListener('click', () => {
  console.log('Clicked!');
});
```

#### Form Submit Event
Fires when a form is submitted, either by clicking a submit button or pressing Enter. This is where you typically validate form data before sending it to a server.

**Example:**
```javascript
const form = document.querySelector('form');

form.addEventListener('submit', function(event) {
  event.preventDefault(); // Prevent default form submission
  
  const formData = new FormData(form);
  const username = formData.get('username');
  
  console.log('Form submitted with:', username);
  // Process form data here
});
```

#### Preventing the default action
Many HTML elements have default behaviors (like forms submitting to a new page, links navigating, etc.). `preventDefault()` stops these default actions so you can handle them with JavaScript instead.

**Example:**
```javascript
// Prevent form from submitting normally
form.addEventListener('submit', function(event) {
  event.preventDefault();
  // Now you can handle submission with JavaScript
});

// Prevent link from navigating
link.addEventListener('click', function(event) {
  event.preventDefault();
  // Custom navigation logic here
});
```

#### Custom Events
You can create and dispatch your own events beyond the built-in browser events. This allows different parts of your application to communicate with each other.

**Example:**
```javascript
// Create a custom event
const customEvent = new CustomEvent('myCustomEvent', {
  detail: { message: 'Hello from custom event!' }
});

// Listen for the custom event
document.addEventListener('myCustomEvent', function(event) {
  console.log(event.detail.message);
});

// Dispatch (trigger) the event
document.dispatchEvent(customEvent);
```

### Data Structures

#### Objects 
Generally everything in JS is an object. Objects hold key-value pairs and are used to represent data structures. They're like containers that store related information together.

**Example:**
```javascript
// Object literal
const person = {
  name: "John Doe",
  age: 30,
  email: "john@example.com",
  greet: function() {
    return "Hello, " + this.name;
  }
};

// Access properties
console.log(person.name); // "John Doe"
console.log(person['age']); // 30
person.greet(); // "Hello, John Doe"

// Add/modify properties
person.city = "New York";
person.age = 31;
```

#### Arrays
Arrays are ordered lists of values stored in a single variable. They use numeric indices (starting at 0) to access elements. Arrays are perfect for storing collections of similar items.

**Example:**
```javascript
// Array creation
const fruits = ["apple", "banana", "orange"];
const numbers = [1, 2, 3, 4, 5];

// Access elements (zero-indexed)
console.log(fruits[0]); // "apple"
console.log(fruits[1]); // "banana"

// Array methods
fruits.push("grape"); // Add to end
fruits.pop(); // Remove from end
fruits.length; // Get array length

// Iterate through array
fruits.forEach(fruit => console.log(fruit));
```

#### JSON 
JavaScript Object Notation (JSON) is a text format for storing and exchanging data. It combines objects and arrays in a structured way. JSON is extremely common and used by many frameworks and systems for data transfer.

**Example:**
```javascript
// JSON string (how data is transmitted)
const jsonString = '{"name":"John","age":30,"hobbies":["reading","coding"]}';

// Parse JSON string to JavaScript object
const person = JSON.parse(jsonString);
console.log(person.name); // "John"

// Convert JavaScript object to JSON string
const personObj = { name: "Jane", age: 25 };
const json = JSON.stringify(personObj);
console.log(json); // '{"name":"Jane","age":25}'
``` 

#### Local Storage
Local storage is a browser API that allows for persistent storage on a domain via key-value pairs. Data persists even after the browser is closed, making it useful for saving user preferences or temporary data.

**Example:**
```javascript
// Save data
localStorage.setItem('username', 'john_doe');
localStorage.setItem('settings', JSON.stringify({ theme: 'dark' }));

// Retrieve data
const username = localStorage.getItem('username');
const settings = JSON.parse(localStorage.getItem('settings'));

// Remove data
localStorage.removeItem('username');

// Clear all data
localStorage.clear();
```

## SQLite
SQLite is a lightweight, file-based database system that doesn't require a separate server. It stores data in a single file and is perfect for small to medium applications. SQLite uses SQL (Structured Query Language) to manage data.

**Key Concepts:**
- **Database**: A single file containing all your data
- **Tables**: Structures that organize data into rows and columns
- **SQL Queries**: Commands to create, read, update, and delete data

**Example SQL:**
```sql
-- Create a table
CREATE TABLE users (
  id INTEGER PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE
);

-- Insert data
INSERT INTO users (name, email) VALUES ('John Doe', 'john@example.com');

-- Query data
SELECT * FROM users WHERE email = 'john@example.com';

-- Update data
UPDATE users SET name = 'Jane Doe' WHERE id = 1;

-- Delete data
DELETE FROM users WHERE id = 1;
```

### PocketBase
PocketBase is a lightweight backend-as-a-service that includes SQLite database, authentication, file storage, and a REST API. It's perfect for quickly building web applications without setting up a complex server infrastructure.

**Key Features:**
- Built-in SQLite database
- User authentication and authorization
- File uploads and storage
- Real-time subscriptions
- Admin dashboard
- RESTful API

**Example Usage:**
```javascript
// Connect to PocketBase
const pb = new PocketBase('http://localhost:8090');

// Authenticate user
await pb.collection('users').authWithPassword('email@example.com', 'password');

// Create a record
const record = await pb.collection('posts').create({
  title: 'My Post',
  content: 'Post content here'
});

// Fetch records
const records = await pb.collection('posts').getList(1, 20);
```

## Docker and containerizing

### Containers
Containers are isolated environments that package an application with everything it needs to run (code, runtime, libraries, settings). They're like lightweight virtual machines that share the host operating system but keep applications separate.

#### Jailed Process
A jailed process is a containerized application that runs in isolation from the host system. It can only access resources (files, network, etc.) that are explicitly granted to it, providing security and preventing conflicts between applications.

#### Name Spacing
Namespacing in Docker isolates container resources (processes, network interfaces, file systems) so containers can't see or interfere with each other. Each container has its own namespace, even though they share the same host operating system.

#### Resource Control Groups
Resource control groups (cgroups) are a Linux kernel feature used by Docker (and other container systems) to limit, account for, and isolate the resource usage (CPU, memory, disk I/O, etc.) of a group of processes. In containers, cgroups ensure that each container only uses its allocated resources and cannot starve the host or other containers, helping to maintain stable and efficient system operation.

### Docker Compose
Docker Compose is a tool for defining and running multi-container Docker applications. Instead of running multiple `docker run` commands, you define all services in a YAML file and start everything with one command.

**Example docker-compose.yml:**
```yaml
version: '3.8'
services:
  web:
    image: nginx
    ports:
      - "80:80"
  database:
    image: postgres
    environment:
      POSTGRES_PASSWORD: mypassword
```

**Commands:**
```bash
docker-compose up    # Start all services
docker-compose down  # Stop all services
```

### Kubernetes
We lightly touched on Kubernetes in this course to show what the next level of how container infrastructure is implemented.

### Parts of a Kubernetes Cluster

#### Node
A server (physical or virtual) that runs containerized applications. There are two types: master/control plane nodes and worker nodes.

#### Pod 
The smallest deployable unit, typically a single container or a group of tightly coupled containers running on a node.

#### Cluster
A set of nodes managed together, running containerized workloads.

#### Control Plane (Master)
Manages the Kubernetes cluster. It makes global decisions (like scheduling) and responds to cluster events.

##### kube-apiserver
Frontend of the control plane that handles all API requests.

##### etcd
Consistent and highly available key-value store used for all cluster data.

##### kube-scheduler 
Assigns Pods to nodes based on resources and constraints.

##### kube-controller-manager 
Runs controllers to handle routine cluster functions (like creating pods, managing replication).

#### Worker Node Components
  ##### kubelet
  Agent on each worker node that runs and manages containers as instructed by the control plane.

  ##### kube-proxy
  Manages network routing and load balancing for services on each node.

  ##### Container Runtime
  Software (like Docker or containerd) that runs containers on the node.

#### Namespace
Logical partition within a cluster, allows organizing resources for different teams or projects.

#### Service
Defines a stable network endpoint to access a group of pods, enabling load balancing and service discovery.

#### Deployment
Ensures a specified number of identical pods are always running, manages rolling updates.

#### Ingress
Manages external access to services, usually using HTTP, provides routing and load balancing.

These components work together to deploy, scale, and manage containerized applications in production.

## NodeJS
Node.js is a JavaScript runtime that allows you to run JavaScript on the server (outside the browser). It's built on Chrome's V8 JavaScript engine and enables building full-stack web applications using JavaScript for both frontend and backend.

### NPM
NPM (Node Package Manager) is the default package manager for Node.js. It allows developers to easily install, manage, and share JavaScript libraries and tools from the npm registry. With NPM, you can add dependencies to your project, run scripts, and manage your project's configuration using the `package.json` file.


### Express
Express is a minimal and flexible web application framework for Node.js. It simplifies building web servers and APIs by providing tools for routing, handling requests, and managing middleware.

**Example:**
```javascript
const express = require('express');
const app = express();

// Middleware to parse JSON
app.use(express.json());

// Route handler
app.get('/', (req, res) => {
  res.send('Hello World!');
});

// Start server
app.listen(3000, () => {
  console.log('Server running on port 3000');
});
```

### SSL
SSL (Secure Sockets Layer) and its successor TLS (Transport Layer Security) are protocols that encrypt data transmitted between a web browser and server. This protects sensitive information from being intercepted. Websites using SSL/TLS show "https://" instead of "http://" and display a padlock icon.

### HTTP and HTTPS
- **HTTP** (HyperText Transfer Protocol): The standard protocol for transferring web pages. Data is sent in plain text, making it vulnerable to interception.
- **HTTPS** (HTTP Secure): HTTP with SSL/TLS encryption. All data is encrypted, providing security for sensitive information like passwords and credit card numbers. Modern websites should use HTTPS.

### Certificate Authority
A Certificate Authority (CA) is a trusted organization that issues digital certificates to verify website identities. When you visit an HTTPS website, your browser checks the site's certificate against a CA to ensure the site is legitimate and the connection is secure. Popular CAs include Let's Encrypt, DigiCert, and GlobalSign.

### REST Endpoints
REST (Representational State Transfer) endpoints are URLs that represent resources in a web API. Each endpoint corresponds to a specific operation (GET, POST, PUT, DELETE) on a resource. REST APIs follow standard conventions for building web services.

**Example:**
```javascript
// Express REST endpoints
app.get('/api/users', (req, res) => {
  // GET: Retrieve all users
  res.json({ users: [...] });
});

app.post('/api/users', (req, res) => {
  // POST: Create a new user
  const newUser = req.body;
  // ... save user
  res.json({ success: true });
});

app.put('/api/users/:id', (req, res) => {
  // PUT: Update user by ID
  const userId = req.params.id;
  // ... update user
  res.json({ success: true });
});

app.delete('/api/users/:id', (req, res) => {
  // DELETE: Remove user by ID
  const userId = req.params.id;
  // ... delete user
  res.json({ success: true });
});
```

## Electron
Electron is a framework that allows you to build desktop applications using web technologies (HTML, CSS, and JavaScript). It combines Chromium (the browser engine) and Node.js, enabling you to create cross-platform desktop apps that work on Windows, macOS, and Linux.

**Key Concepts:**
- **Main Process**: The Node.js process that controls the application lifecycle
- **Renderer Process**: Browser windows that display your HTML/CSS/JS
- **IPC (Inter-Process Communication)**: How the main and renderer processes communicate

**Example Structure:**
```javascript
// main.js (Main Process)
const { app, BrowserWindow } = require('electron');

function createWindow() {
  const win = new BrowserWindow({
    width: 800,
    height: 600,
    webPreferences: {
      nodeIntegration: true
    }
  });
  
  win.loadFile('index.html');
}

app.whenReady().then(createWindow);
```

Popular Electron apps include VS Code, Slack, Discord, and many others.
