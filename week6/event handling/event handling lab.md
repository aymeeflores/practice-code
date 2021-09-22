Lab: Event Handling in React
Instructions
Create a component called AddTodo. This component should have a form with a textbox and a button. Clicking on the button should log out whatever the user typed into the textbox. Add this component to your top level App component.

In your App component, add an array to the state called todos which will hold a list of todo objects. Add 2 - 3 todo objects to start, the structure of each todo will look like the following:

// example Todo
let todo = {
id: 9,
content: "finish this lab",
done: false
}
In the render function, loop/map over the array of todos and output them to the screen as <li> elements.

Create a handler in the App component that adds a new todo to the list of todos in state. Pass this handler to AddTodo as a prop. Update AddTodo to add whatever the user typed into the textbox as a new todo. When the user clicks the button, the textbox should be cleared, and the new todo should show up in the list.
