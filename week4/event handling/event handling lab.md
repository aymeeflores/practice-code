Lab: Event Handling & Asynchronous
Getting Started
To begin, download the starter files here.

Using DOM API, find the right event and understand how to use them for following exercise. We will focus on click and keypress events.

Click Events
Add an onclick listener to the window and log the event.target property. Depending on where you click in window, you will see that element printed in console.

Add an onclick listener to the Logo and bold the logo text by applying a style. Refer to DOM Style API to see how to accomplish this task.

Keypress Events
Find the search textbox using querySelector and attach a keyup event listener to it using addEventListener. Find the Hero Title element using querySelector and change the innerHTML of it to be the key (event.key) that was pressed.
Repeat the process by also getting the Content element and changing the innerHTML to the value of the search element (event.target.value).
