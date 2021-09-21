Lab: Building Components with JavaScript
Getting Started
In this lab you will be starting with the BrainStation template that you are familiar with. The starter has already turned the body of the page into a large component for you.

To get started, please download the starter files here.

Instructions
Open index.html and take a look at its appearance in the browser

Identify the visual components
Which components are nested inside other components?
Do you think that there is a single answer to this question?
Currently our HTML is rendered as one big string in script.js. Let’s create a class component for each of the sub components. Altogether, you should have a Header, Hero, MainContent & Footer components.

For each of your chosen components:

Identify the portion of HTML to be rendered inside of that component. You will have to cut & paste the relevant HTML for that component from the big HTML string provided to you.
Create a new class with the render method and put your component’s HTML inside of it.
Use the render() method of your new class to append your HTML to the main component that is already provided to you using innerHTML.
Be careful about the order in which you define your classes and append to innerHTML of the main component.
No hoisting for classes!
Think about some challenges faced, potential bottlenecks, and improvements for your implementation. We will use React going forward to create components so it’s good to reflect on current pain points to better understand how React will help us solve all the challenges faced by using just plain old JavaScript.
