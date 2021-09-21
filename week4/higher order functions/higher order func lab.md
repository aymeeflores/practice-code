Lab: Higher Order Functions
Getting Started
In this lab you will be writing code in the script.js file, and running it by opening index.html in the browser or by refreshing the page. Check your results (or errors) in the Chrome Dev Tools console. To keep your lab more organized you might like to put each exercise inside its own function.

To get started, please download the starter files here.

Instructions
Part 1: Create Your Own Higher-order Function That Takes a Function
Write a function called output that:

Takes a string parameter
Also takes a function parameter
Invokes the passed function with the passed string as its only parameter
Test your function by:

Passing console.log as the function parameter
Passing alert as the function parameter
Passing your own custom function, for example create a function that appends “Output String: “ to a string parameter passed to it
The goal is to understand the difference between passing function as an argument (as a function object) vs. invoking a function to run it (using parentheses).

Also feel free to add extra console.logs or breakpoints (helps practice your debugging skills) to understand order of execution for code.

While it might feel weird passing functions around as arguments to other functions at first, practice being comfortable with the concept as it is one of fundamental concepts that will be used constantly going forward.

Part 2: Create Your Own Higher-order Function That Returns a Function
The function will be called isEqualTo

It will take a single string parameter
It will return another function
The returned function will:
Take a single string parameter
Compare the passed string to the string passed to isEqualTo and return true if they are equal, otherwise false
To test your function:

Choose a test string
e.g. "coffee"
Call isEqualTo and store the function that it returns in a variable (eg. isEqualToCoffee)
Just like passing functions as arguments, returning functions is a fundamental concept to grasp. Functions have inputs (parameters) and outputs (return values). Both parameters and return values can be other functions. We typically save return values of a function in a variable, and the same can be done for a returned function.
Call the returned function with values that you expect to produce true and false
Use console.log to see the results
Calling your isEqualToCoffee function with “coffee” should return true, calling it with anything else should return false
Part 3: Array Methods
Create a array of at least 3 strings with types of bugs

E.g. “ladybug”, “stinkbug”, “beetle”
Include one item in the array that is not a bug

E.g. “latte”
console.log your array for inspection

Use the filter array method to create an array that only contains bugs and assign it to a new variable

Generate a function using your previously created HOF (Higher Order Function) isEqualTo to make your comparison
Think of the most efficient comparison function, should it be the one performing a comparison with the bug strings or latte?
Consult MDN's documentation for the filter method usage and think of the way you can use your generated function to do the filtering
console.log your original and filtered arrays for inspection

How many items do you expect to remain in the filtered array?
Has your original array changed?
Use map to concatenate "is a bug" to each of the bug strings in the filtered array and assign it to a new variable

Has your filtered array changed?
Use forEach to print out each of the concatenated strings using the output function that you wrote in the first exercise

Try using console.log directly in forEach callback, does it work? Why or why not?
