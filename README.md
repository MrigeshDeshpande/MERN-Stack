# MERN-Stack
Learning and Exploring MERN stack


MERN stands for MongoDB, Express, React, Node, after the four key technologies that make up the stack.

MongoDB - document database
Express(.js) - Node.js web framework
React(.js) - a client-side JavaScript framework
Node(.js) - the premier JavaScript web server

![image](https://user-images.githubusercontent.com/67750918/182497123-6b7282a0-7fa5-4442-9658-6f43028cdf21.png)

The middle (application) tier is made up of Express and Node. Node.js is a popular and capable JavaScript server platform, while Express.js is a server-side web framework. Regardless of the form you pick, ME-(RVA)-N is the best method to work with JavaScript and JSON from start to finish.

## How does the MERN stack work?

The MERN stack's top layer is React.js, a declarative JavaScript framework for developing dynamic client-side HTML applications. React allows you to create sophisticated interfaces by connecting basic Components to data on your backend server and rendering them as HTML.

### React.js Front End

React excels at managing stateful, data-driven interfaces with minimum code and suffering, and it includes all the bells and whistles you'd expect from a modern web framework: outstanding support for forms, error handling, events, lists, and more.

### Express.js and Node.js Server Tier

The Express.js server-side framework, which runs within a Node.js server, is the next level below. Express.js touts itself as a "fast, unopinionated, simple Node.js web framework," and that is precisely what it is. Express.js has robust models for URL routing (which matches an incoming URL with a server function) and managing HTTP requests and answers.

You may connect to Express.js functions that power your application by sending XML HTTP Requests (XHRs), GETs, or POSTs from your React.js front-end. These methods, in turn, leverage MongoDB's Node.js drivers to access and update data in your MongoDB database, either via callbacks or Promises.

### MongoDB Database Tier

If your application maintains data (user profiles, content, comments, uploads, events, and so on), you'll need a database that's as simple to use as React, Express, and Node.

That's where MongoDB comes in: JSON documents generated by your React.js front end may be transmitted to the Express.js server, where they can be processed and (if valid) saved straight in MongoDB for subsequent retrieval. Again, if you're working on the cloud, Atlas is a good place to start. Continue reading if you want to put up your own MERN stack!

So, lets get started with setting up the Environment
------

To get started, you will need to do the following:
- **Install Node**
    - To install Node, go to https://nodejs.org/en/ and download either the LTS version or the current version.

- **Have or Install a Code Editor**
    - You can use any code editor of your choice for this tutorial. However, for the sake of demonstration, we will be using VS Code editor with the plugin prettier and vscode icons.

MERN enables us to build full-stack solutions. So, in order to fully realise its potential, we will develop a MERN stack project. We will develop both a back end and a front end for this project. The front end will be built with React, while the back end will be built with MongoDB, Node, and Express. We shall refer to the front end client and the back end server.

## What is NodeJS?

- ​ A JavaScript Runtime Environment 
- ​ Built on Chrome's V8 Engine! 

- ​ Light, scalable and open-source language platform 

- ​ Used for Server-side development

- ​ Since we use Javascript in both the frontend and backend the development will be much faster.

Hello World in NodeJS
------
1. Create a file - helloworld.js
```Javascript 
console.log(“Hello World”);
```
2. And save the file after adding this line
3. Run the file - `node helloworld.js`

NodeJS in-built package
------
- Modules are the blocks of encapsulated code that communicates with an external application on the basis of their related functionality. 

- Modules can be a single file or a collection of multiples files/folders. 

-  The reason programmers are heavily reliant on modules is because of their re-usability as well as the ability to break down a complex piece of code into manageable chunks.

Modules are of three types:
------
- ->Core Modules
- ->Local Modules
- ->Third-party Modules

Core Modules:
------
**Syntax:**

`var module=require('module_name');`

 local modules are created locally in your Node.js application

The require() function will return a JavaScript type depending on what the particular module returns. The following example demonstrates how to use the Node.js Http module to create a web server.
```Javascript
var http = require('http');
http.createServer(function (req, res) {
res.writeHead(200, {'Content-Type': 'text/html'});
res.write('Welcome to this page!');
res.end();
}).listen(3000);
```

 **The following list contains some of the important core modules in Node.js:**
![image](https://user-images.githubusercontent.com/67750918/182500723-757b315d-9627-46ba-80c2-4a0b6d27669f.png)

-------
Local Module:
------
- Local modules are modules created locally in your Node.js application. 

- These modules include different functionalities of your application in separate files and folders. 

- The module.exports is a special object which is included in every JS file in the Node.js application by default. Use module.exports or exports to expose a function, object or variable as a module in Node.js.

- The require() function returns a log object because logging module exposes an object using module.exports
- - - - - 
Let’s create a simple calculating module that calculates various operations. Create a calculator.js file that has the following code:

*FileName: Calculator.js*
```Javascript
exports.add = function (x, y) {
	return x + y;
};
	
exports.sub = function (x, y) {
	return x - y;
};
	
exports.mult = function (x, y) {
	return x * y;
};
	
exports.div = function (x, y) {
	return x / y;
};
```
Since this file provides attributes to the outer world via exports, another file can use its exported functionality using the require() function.

*FileName: index.js*
``` Javascript
var calculator = require('./calc');
	
var x = 50, y = 10;
	
console.log("Addition of 50 and 10 is "
				+ calculator.add(x, y));
	
console.log("Subtraction of 50 and 10 is "
				+ calculator.sub(x, y));
	
console.log("Multiplication of 50 and 10 is "
				+ calculator.mult(x, y));
	
console.log("Division of 50 and 10 is "
				+ calculator.div(x, y));

```

Step to run this program: Run index.js file using the following command:
```
node index.js
Output:

Addition of 50 and 10 is 60
Subtraction of 50 and 10 is 40
Multiplication of 50 and 10 is 500
Division of 50 and 10 is 5
```
Third-party Modules
------
- Node 3rd party modules is a module or package which is developed and manitained by 3rd parties.

- Millions of 3rd party node modules/packages which are freely available on NPM Registry.

- You can install node 3rd party modules/packages and use them to add functionality to your projects.

- Node 3rd party modules can be installed using NPM (Node Package Manager).

*Example:*
```Javascript
npm install express
npm install mongoose
```

NPM
(Node Packet Manager)
------
npm is the Node JavaScript platform's package management. It instals modules so that nodes can locate them and intelligently resolves dependency issues. It is highly customizable to serve a wide range of use cases. It is most widely used for publishing, discovering, installing, and developing node applications.
Default package manager for the Node.js environment, makes it easier for a developer to publish and share the source code of Node.js packages npm can manage dependencies.

npm can (in one command line) install all the dependencies of a project.
Dependencies are also defined in package.json.

