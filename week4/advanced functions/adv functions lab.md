Lab: Advanced Functions
Getting Started
This lab will be completed by You writing your code in script.js and run it by opening index.html in the browser (or refreshing the page).
Make sure to open the web inspector to see your errors and logs in the console
Note: Argument vs Parameter
It is important to remember the distinction between an argument and a parameter. While these terms are often used interchangeably, there is a difference.

When defining a function, the variables within the parentheses are parameters.

// param1 and param2 are parameters here
function myFunc(param1, param2) {
}
When invoking a function, the variables passed to the function are arguments.

let someVar = 'hello';
myFunc(someVar); // someVar is considered an argument here
Exercises
Named Functions as Parameters
Write a function that...

Takes one string parameter
Concatenates the passed string with Your name is:
console.logs the result
Assign the function to a variable called outputName

Write a function called sayMyName that...

Takes two string parameters (first name and last name) and one function parameter
Concatenates the first name and last name into a single string
Invokes the function passed in as a parameter, passing the newly concatenated string as an argument to it
Call sayMyName with your outputName function as the function parameter

Call sayMyName with console.log as the function parameter

What do you expect the result to be of each call?
Anonymous Functions as Parameters
Use the setTimeout function to console.log a message of your choice after 2 seconds

Recall that setTimeout takes two parameters
A function to be invoked
The number of milliseconds to wait before invoking
Make the function parameter of your setTimeout call an anonymous function
Modify the anonymous function passed to setTimeout to call sayMyName instead of console.log after 2 seconds

You should call sayMyName in the same way you did in step 4 of the last exercise
Arrow Functions
Rewrite the previous exercise with the arrow function syntax
