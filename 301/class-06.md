# Node.js
Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.  Or an event-based, non-blocking, asynchronous I/O (input/output) runtime that uses Google’s V8 JavaScript engine and libuv library.
- The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.
  - That doesn't mean that Node programs are executed in a browser.
  - Rather, the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.
- This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.  

## Node Binaries vs Version Manager
 Version Manager is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.

 ## Node.js Has Excellent Support for Modern JavaScript
 Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers.
 ## npm
 JavaScript Package Manager- Node comes bundled with this package manager called npm.  It is also the world’s largest software registry, with over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week.
 ## What Is Node.js Used For?
 ***npm is for installing and Node.js is for running various build tools, and designed to automate the processs of developing a modern JS application.***
 -  These build tools come in all shapes and sizes, and can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.
   - If you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm.
     - These frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.
## Node.js Lets Us Run JavaScript on the Server
One of the biggest use cases for Node.js — running JavaScript on the server.
## The Node.js Execution Model
Node.js is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event.
  - When a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the ***libuv*** library to implement this asynchronous (that is, non-blocking) behavior.
  - Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has a built-in module to help you implement a cloning strategy on a single server.  
  ![***Node's Execution model:***](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png)
  ## Limitations
  - Blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.
  - Some developers also dislike the callback-based style of coding that JavaScript imposes.
  ## What Kind of Apps Is Node.js Suited To?
  - Applications that require some form of real-time interaction or collaboration.  Like chat sites, or apps where you can watch a document being edited live by someone else.
  - Applications where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded.
  ## Advantages of Node.js
  - Speed and scalability.
  - No need to switch modes, meaning you can do everything in the same language, which is more productive, and facilitates the ability to share code between server and client.
  - Another of Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and it is a common for interacting with object databases even between the different languages.  
    - JSON is ideally suited for consumption by a JavaScript program, meaning that when you’re working with Node, data can flow neatly between layers without the need for reformatting. You can have one syntax from browser to server to database.
- JavaScript is ubiquitous: most programmers are familiar with it, or have used it at some point. This means that transitioning to Node development is potentially easier than to other server-side languages. 
## Other Uses of Node
- It can be used as a scripting language to automate repetitive or error prone tasks on your PC.
- It can also be used to write your own command line tool, to scaffold out new projects.
- Node.js can also can be used to build cross-platform desktop apps and even to create your own robots.