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

## Synchronous & Asynchronous programming

Synchronous
------
Synchronous, in general, means one at a time.
Synchronous is the sequential flow of program execution in a programming
context.

The program/code will be read in sequence from top to bottom and
executed line by line, with one thing getting executed at a time.
The Javascript engine waits for the code to get executed completely before
moving to the next line.
So Synchronous programming executes each line of code at a time in a
sequence

Example:
```Javascript
	console.log('Hi');
	function greet(){
	 console.log('Welcome to
	Grandline');
	}
	greet();
	// Hi
	// Welcome to Grandline
```
Asynchronous
------
Asynchronous, in general, is not occurring at the same time. 
Asynchronous in a programming context is the execution of code/function without waiting for the other code/functions to execute. 
This enables the Javascript engine to execute the code without halting the code execution process

In Javascript, there are different ways to achieve asynchronous execution.

Callbacks:

We need to note that Callbacks are used inside Browser API/Web API functions or events.
These APIs internally accept callback functions to achieve asynchronous programming. They have
methods such as setTimeout and event handlers like click, mouse over, scroll, etc.

Callbacks are functions that are passed as arguments to other functions and
then invoked in the outer function to perform its operation.
Also, callbacks take time to execute and are not executed immediately; they
are passed at first and are invoked later.

Callbacks should be implemented asynchronously. Else the event loop in the
JS engine has to wait until the callback is executed, which may cause
undesired output, or our program may become unresponsive.

```Javascript
	function greet(callbackFn){
	 callbackFn();
	 console.log('Welcome to
	Grandline');
	}
	greet(function(){
	 console.log('Hi')
	});
	// Hi
	// Welcome to Grandline
```

```Javascript
	// Same code with arrow syntax
	function greet(callbackFn){
	 callbackFn();
	 console.log('Welcome to
	Grandline');
	}
	greet(() => console.log('Hi'));
	// Hi
	// Welcome to Grandline
```

Call Stack
------

Call Stack is the stack data structure maintained by the Javascript engine. It
operates in a LIFO manner (Last in First Out). It has the purpose of tracking
the current function being executed. Call Stack is also known as Function
execution stack.

When the Javascript engine runs the code, the first thing that happens
is an execution context is created precisely Global Execution Context
(GEC) whenever the code execution is started.
- So the first thing that’s pushed into the call stack is GEC.
- After the execution of code, the execution context is popped out.
- Remember, each function has its execution context.
-Execution context is the environment in which the code is executed
Example:
```Javascript
	function greet(){
	 return function() {
	 console.log('Welcome to Grandline');
	 }
	}
	const result = greet();
	result(); // Welcome to Grandline
```

Callback queue
------

Callback functions do not enter the call stack for execution directly instead a
callback function is registered in the Web API and then the result of callback
is stored now the callback is entered to Callback Queue. 

It is a queue data structure that has entries in FIFO manner (First in First out) and stores all
the callback functions ready for execution and once the call stack is empty
they are deleted from the queue and pushed to the stack for execution

Callbacks with Async Example:
```javascript
console.log('Hi');
function callback(){
 console.log('Welcome to Grandline');
}
setTimeout(callback, 2000);
console.log('Join our Pirate Crew & be our Nakama');
// Hi
// Join our Pirate Crew & be our Nakama
// Welcome to Grandline (with a delay of 2 seconds)

```
CallBacks hell
------

- It is a common scenario to have nested callbacks and all the
nested callbacks will wait inside the callback queue and be pushed to the call stack in
FIFO manner (First in First out).
- This complex nesting of callbacks makes our code difficult to maintain and debug.
- It is also prone to more errors if not written carefully.
- This scenario in which we have complex nested callbacks is referred to as Callback hell.
Here, each callback takes arguments that are the result of previous callbacks.
- This kind of callback structure forms a pyramid like structure

Example
```Javascript
	// Callbacks hell example
	function cheese(){
	 console.log('Add lots of cheese');
	}
	function patty(cheese){
	 console.log('Add veggies and patties');
	 cheese();
	}
	function bun(patty){
	 console.log('Take two fresh buns');
	 patty(cheese);
	}
	function burger(bun){
	 setTimeout(() => {
	 bun(patty);
	 console.log('Our Burger is ready');
	 }, 2000);
	}
	burger(bun);
	console.log('Lets make a Burger');
	
	//Output:
	
	// Lets make a Burger// (after delay of 2000ms)
	// Take two fresh buns
	// Add veggies and patties
	// Add lots of cheese
	// Our Burger is ready
```
Timers in JS
------
In Javascript there are two Timing Events:
● setTimeout()
● setInterval()

setTimeout()
------

setTimeout(): It is basically a function that is used to execute a function or code after a specified delay.
`Syntax: setTimeout(function, milliseconds, args)`
Example:
```javascript
	function burger(){
	 setTimeout(() => {
	 console.log('Our Burger
	is ready');
	 }, 2000);
	}
	burger();
	// (after delay of 2 seconds)
	// Our Burger is ready
```
clearTimeout()
------

clearTimeout() is the method used to cancel/clear the timeout even before it is
executed.
- It accepts the variable to which we assign the setTimeout(). This variable
returns the reference of setTimeout(). Here we use clearTimeout(getFood)
with getFood variable.
- It does not clear/cancel the delay in the setTimeout it actually cancels the
setTimeout() event itself.
```javascript
	const getFood = setTimeout((food) => {
	 console.log('Our ' + food +' is ready');
	}, 2000, 'Pizza');
	clearTimeout(getFood);
	// Nothing happens and code just exits
```

setInterval()
------
setInterval(): It is basically a function that is used to execute a function or code repeatedly after a
specified interval of time.
`Syntax: setInterval(function, milliseconds, args)`
Example:
```javascript
	setInterval((food) => {
	 console.log('Our ' + food +' is ready');
	}, 2000, 'Pizza');
	// Gets logged every 2 seconds
	// Our Pizza is ready
	// Our Pizza is ready
	// Our Pizza is ready
	// Our Pizza is ready
	// Our Pizza is ready
	// ^C
```
clearInterval()
------
clearInterval() is the method used to stop/clear the interval.
- It accepts the variable more precisely intervalID to which we assign the
setInterval(). Here we use clearInterval(getFood) with getFood variable to stop
the setInterval().
- It does not clear the delay in the setInterval. It actually stops the setInterval()
event itself before execution

```Javascript
	const getfood = setInterval((food) => {
	 console.log('Our ' + food +' is ready');
	}, 2000, 'Pizza');
	clearInterval(getfood);
	// Nothing happens and code just exits
```
Promises: 
Promises are objects in JS that let us perform asynchronous operations.

An object that represents the
completion (or failure) of an
asynchronous operation and also its
resulting value is known as a promise.
```javascript
	const newPromise= new Promise((resolve, reject)=>{
	console.log("Promise created");
	setTimeout() => {
	reject ("Some Error");
	), 1000); //reject after 1 sec

	console.log("Exit from promise")
	});

	console.log("First txt in sync");
	
	newPromise
	.then((result) => {
	console.log("success: ", result);
	})
	.catch((error) => { 
	console.log("Faliure:", error);
	})
	.finally (() => {
	console.log("Promise completed");
	});
	
	console.log("Last txt sync");
```
## Promise Hell

Promise hell is a self created
problem due to lack of
understanding of Promises,
unlike callback hell. In Promise
hell as well we have to wait for
other promises to return and it
will fill the stack.
```javascript
	fetchStory()
	.then((story) => { return findText (story);
	})
	.then((txt) => {
	return print (txt);
	});

	//single liners
	fetchStory (
	.then((story) => findText (story))
	.then((txt) => print(txt));

	// inline
	fetchStory()
	.then (findText)
	.then (print);
```
## Async/Await: 

Async Await keywords were introduced in Javascript in ECMAScript 2017. This made
asynchronous programming easier and is considered a better alternative to promises

Async/ Await is used to handle promises in
synchronous code fashion with less code
effort.

Async: We put this keyword before any
function then, it will return a promise.

Await: This keyword is used before a promise
inside the Async block to block the code until
promise resolves or reject.

So, these keyword helps us to get write a
synchronous fashion code with cleaner syntax.

Example:
```Javascript
const first = ()=> new Promise(resolve =>{
setTimeout(() => resolve ('first ()'), 1000);
});
const second () => new Promise (resolve => { 
setTimeout(() => resolve('second ()'), 1000);
});
const third =() => new Promise(resolve -> {
setTimeout(() => resolve('third ()'), 1000);
});

//First Apporach -->Asynchronous

Promise.all([first(), second (), third (),(someKey:someValue }]}
.then((data) => {
console.log("success:", data);
})
.catch((err) => {
console.log("error:", err);
})

//Second Approach -->Synchronous

const process = async () => {
const first await a();
const second = await b();
const third = await c();

return [first, second, third];	
};

process
	.then((data)=>{
	console.log("success:",data);
	})
	.catch((err)=>
	{
		console.log("error:",err);
	})
```


