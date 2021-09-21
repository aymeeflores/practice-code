DOM Event Handling Practice
Overview
The purpose of this challenge is to get you familiar with manipulating the DOM using Javascript. The task is to allow a user to submit some text and have their submission appear on the screen. Please download the starter code needed here.

Directions
To use Javascript with our HTML and CSS, we will need a JS file and import into our HTML file using a script tag. Remember, the script tag show be at the bottom of our body.

First, create a click event handler on the button with an id of submitBtn.

Inside the event handler:

Test that your event handler is registered by using console.log() to log some output.
Use the event.preventDefault() method to prevent the page from reloading on submit.
use the DOM API to create an li element and assign it to a variable called item.
Grab the value from the text input and store it in a variable.
Set the text for the item element to the value from text input.
using the DOM API get a reference to the ul element with the id of list and append your newly created item element to it's children.
Finally, clear the text from the input field.
Diving Deeper:

Try to stop the user from entering an empty string.
Using classes and CSS, try to add an animation when a new list item is created
