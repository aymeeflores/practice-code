ab: Objects & Constructors
Getting Started
In this lab you will be writing code in script.js and running it by opening index.html in the browser or refreshing the page. Check your results (or errors) in the Chrome inspector. To keep your lab more organized, you might like to put each exercise inside its own folder.

To get started, please download the starter files here.

Exercises
Write a Burger() constructor that will create burger objects. Each burger will have the following properties:

toppings: an array of string values for each burger topping
protein: a string indicating the burger's type of protein
containsGluten: a boolean indicating if the burger is gluten-free
describe: a method that prints a description of the protein and toppings
Create two instances/objects using the Burger() constructor. When creating each new Burger, try adding different toppings and proteins, along with varying the gluten-free status.

console.log the two instances/objects to your browser's console to inspect their properties

Note the properties that you set in the constructor
Toppings, protein, containsGluten, describe
Also note the prototype property that was added automatically
Add to the Burger() prototype a warning method that:

Prints a warning if the burger contains gluten
Prints a 'gluten-free' message if it does not contain gluten
Check that the two previously created burgers print the correct message when invoking warning()

console.log your burgers again

Note that the prototype property now holds a reference to the warning() method
