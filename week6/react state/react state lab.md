Lab: React State
Getting Started
This lab builds upon the previous one. You may use your own completed lab or get a fresh start with the starter code here.

Storing Data in State
Modify the CardList component to store an array of card contents in the state property of the component.

Make sure to change the references in your template accordingly.
Check that your page still shows the content as expected.

Changing Data State
Data in the state is not very useful unless we can modify it. We will add a button to the cardlist that adds a new item to the list.

Create a function in the CardList component called refreshList that adds a new content object to the content array, you will need to use setState() to do this.
Note that you should never mutate state directly which is why we use setState().
Next, wrap setState() with setTimeout() and set it to 3000 (milliseconds). This will simulate the delay of a network call.

Finally, create a button in the CardList template that has an onClick property which calls .refreshList().

What do you expect to happen to your webpage when you click the button?
What if you click the button multiple times?
What do you expect to happen when you refresh the page?
Tracking Clicks
In the Card component, initialize a state variable called clickCounter to 0.

Write a function called countClick() that increments the clickCounter state variable and then logs the current count.

In the anonymous function passed to the onClick property of the root element, call countClick() before invoking the clickHandler().

What do you expect to see in the console when you click a card?

What do you expect to see when you click a different card?
