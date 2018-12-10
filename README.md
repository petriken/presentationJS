What is a Function?
1. A JavaScript function is a block of code designed to perform a particular task.
2. Functions are executed when they are called. This is known as invoking a function.
3. Values can be passed into functions and used within the function.
4. Functions always return a value. In JavaScript, if no return value is specified, the function will return undefined.
5. Functions are objects.

Define a Function.

There are a few different ways to define a function in JavaScript:
A Function Declaration defines a named function. 
A Function Expressions defines a named or anonymous function.
An Arrow Function Expression is a shorter syntax for writing function expressions

Function Declaration 
To create a function declaration you use the function keyword followed by the name of the function.

Function Expressions 
A Function Expression defines a named or anonymous function.
An anonymous function is a function that has no name

Arrow functions
Arrow functions (also called “fat arrow functions”) are undoubtedly one of the more popular features of ES6. 
Here is a function written in ES5 syntax:

the same  function written as an arrow function:

An arrow function expression not have its own this, arguments or super. Arrow function cannot be used as constructors.

An Immediately-invoked Function Expression (IIFE) is a way to execute functions immediately, as soon as they are created.
This is the syntax that defines an IIFE:
We basically have a function defined inside parentheses, and then we append () to execute that function: (/* function */)().

What is this?
The JavaScript this keyword refers to the object it belongs to.

In most cases, the value of this is determined by how a function is called. It can't be set by assignment during execution, and it may be different each time the function is called.

Global Context
In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.

Function context
Inside a function, the value of this depends on how the function is called.

Simple call
Since the following code is not in strict mode, and because the value of this is not set by the call, this will default to the global object, which is window in a browser. 

In strict mode, however, the value of this remains at whatever it was set to when entering the execution context, so, in the following case, this will default to undefined:

To pass the value of this from one context to another, use call(), or apply():

In arrow functions, this retains the value of the enclosing lexical context's this. In global code, it will be set to the global object:
In arrow functions, this is bound to the environment in which the function was created. In the global scope, this will point to the global object.

As an object method
When a function is called as a method of an object, its this is set to the object the method is called on.
As a constructor
When a function is used as a constructor (with the new keyword), its this is bound to the new object being constructed.
As a DOM event handler
When a function is used as an event handler, its this is set to the element the event fired from 
In an inline event handler
When the code is called from an inline on-event handler, its this is set to the DOM element on which the listener is placed:
Closure
A closure is the combination of a function and the lexical environment within which that function was declared.

In this example displayName() inner function is returned from the outer function before being executed.

Practical closures
• Closures are useful because they let you associate some data (the lexical environment) with a function that operates on that data. 
• Also we can use closures to define public functions that can access private functions and variables
• It is unwise to unnecessarily create functions within other functions if closures are not needed for a particular task, as it will negatively affect script performance both in terms of processing speed and memory consumption.

Function composition 
is a mechanism of combining multiple simple functions to build a more complicated one. The result of each function is passed to the next one until you get a result.

Method chaining is a technique that can be used to simplify code in scenarios that involve calling multiple functions on the same object consecutively.

The typical way to enable method chaining is to return the current object at the end of every function. 

For our example, we will define a custom class with the ability to chain methods
Here is example with method chaining on our new class: 
Here is example without method chaining on our new class: 
By using method chaining we get much cleaner code that is easier to understand
Method chaining can be a very useful technique to have in your programming tools. 

TALK ABOUT THE FUNCTIONS OF JAVASCRIPT CAN BE INFINITE, SO THIS WILL END. THANKS FOR ATTENTION