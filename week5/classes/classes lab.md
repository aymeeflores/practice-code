Student Content
Advanced JavaScript
Classes
Exercises
Lab: Classes
Getting Started
In this lab you will be writing code in the script.js file and running it by opening index.html in the browser or refreshing the page. Check your results (or errors) in the Chrome inspector.

In your last lab (Objects & Constructors) you created a constructor function to make burgers. You are encouraged to use your code from last lab, but starter code is provided here should you prefer to use it.

Instructions
Part 1
Rewrite your Burger constructor as a class

It should take the same three parameters
It should also contain the same two methods
Test your class by constructing the same Burger with the constructor function and the class

Are there any differences when you inspect them in the console?
If there are, do they matter?
How might you change the class to make the two objects the same?
Do all of their methods work in the same way?
Part 2
Create a class called BurgerWithSide that:

Extends the Burger class
Adds a side string property that describes the burger's side dish
Adds a method called friesWithThat() that returns true if the side is "fries", also try using the string method .toLowerCase() for your method to also work if the string is "Fries" e.g. has any uppercase letters
Test your class by constructing a new BurgerWithSide

Test the methods provided by the base Burger class
Test your new friesWithThat() method
The lab starter script.js contains a function called describeAll

It accepts as its only parameter a list of describe functions for it to call
Pass to this function an array containing the describe calls from each of the Burger and BurgerWithSide objects that you have built in this lab
