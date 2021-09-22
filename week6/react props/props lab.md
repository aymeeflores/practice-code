Lab: React Props
Getting Started with React Props and the React Docs
As a developer understanding documentation is a skill that can be just as important as writing code. You will often need to referring to documentation as things change/update. For example, a new release of a library like React may deprecate/remove old features as well as add new features. You may be required to change how you write your React Applications in order to follow best practices and avoid breaking changes.

The React team has an excellent job of documenting the React library! The main tutorial in their documentation shows how to build a Tic Tac Toe Game with "time-travel" features! The Tic Tac Toe tutorial is great, however, it is recommended to start with the Guide to Main Concepts first to fully understand the code.

Before starting todays lab it’s time to do some review of how React Props work. Please start by reviewing the documentation here: Guide to Main Concepts and please read up to section 5, stopping at "State and Lifecycle". This should help you to understand Components and Props before applying the concepts in todays lab and in the future.

Directions
In this lab we will build upon the static site conversion that we started in the previous lab. You may use your own completed lab or get a fresh start with the starter code below. Please download the starter code here

Adding Props to a Component
Modify the Header component to take a logo prop

Use the prop value to set the logo of the header

Add the Header element to the App component template

Make sure to populate the logo prop of your Header element
Creating Arrays of Components with Props
Modify the Card component to take a content prop and a title prop

Use these props in place of the fixed text in the template

In the CardList component create an array of two objects with content and title props

.map() this array to an array of Card components

Add these components to the CardList template

Open your console and note the warning regarding unique keys for your list items

Add an index prop to your Card component and populate it with a unique key inside the CardList template

Adding Functions as Props
Modify the Card component to accept a function prop called clickHandler

Inside of the Card template, pass a function to the onClick prop of the root element that calls the clickHandler

To the clickHandler function it should pass the Event produced by the click as the first parameter
It should also pass the title of the card as the second parameter
Inside the CardList render function, define a function that is designed to receive the Event and title parameters

It should ignore the event parameter and then log the title to the console
Pass this function as the clickHandler prop for each of the Card elements

Test that the title of the card is logged when you click it
