Snowman Game
Introduction
Let's create a simple snowman application using JavaScript to facilitate the logic, and the command line to run a word-guessing game. This exercise uses some technology we haven't covered yet, so there is a small amount of setup required before we start.

Instructions
Step 1: Set Up
Please download the starter code here: Using the command line, navigate to the root folder for this challenge ('Snowman Game Starter Code' folder). Once there, run the command npm install. (This is something we'll cover in more detail later, all you need to know right now is that it will install a package of JavaScript that has prebuilt functionality that we will be using in this project)

Step 2: Problem Solving
Using pseudocode (a high-level look at the flow your program will follow) write out the game logic for snowman.

Be sure to think of things such as:

What do we need to keep track of as the user plays?
What should we do if the user guesses the same letter twice?
How will we check if the letter the user guesses is in our chosen word?
When will the game end?
Step 2: Loops and Conditions
We've written a high level look at how our snowman program should work, but we haven't written any of the logic that will allow us to interact with our snowman app. Let's start by writing the conditions that will handle the letter guessing logic.

Apply some basic array operations that will capture a user input and store it into an array of 'previous guesses' Hint: look up array methods, there may be a few ways to store a value inside an array.
Write some conditional statements that will check whether or not the current guess matches any of the previous guesses that you have stored. You will have to use loops to accomplish this task
In the starter code, go to the place marked 'Part 2 - process guess' and write code to process the user's guess
In addition to checking if the current guess matches previous guesses, add logic to check whether or not the current guess is in the chosen answer. If the user enters a duplicate guess, you should console.log that they've already guessed that
Add console.logs to display the previous guesses made by the user
Step 3: Functions
We've written some logic to check whether or not the current guess matches any previous guesses, but we have yet to add the logic to terminate the game if the win/lose conditions have been met. Using your pseudocode from before, write conditional statements that will correctly terminate the game on a win or loss.

Implement a way to count incorrect guesses made by the user. (Since we are checking the current guess against previous guesses, you should NOT count duplicate guesses as incorrect guesses)
Add conditions that will terminate the game if the user wins (by guessing all the correct letters), or loses (by reaching 6 incorrect guesses)
Using your previous work, as well as your pseudocode, complete the checkGameOver function to return true if the game has been completed
Be sure to consider the control flow of your application when writing these statements, understanding when things happen is crucial when writing programs. Also remember that there is a clear difference between a function calling console.log and that same function returning a value.

Step 4: Creating Objects
Right now, our application has no way of storing the results of all our previous games. We’re going to try to add some very basic methods of storing information to be used later. You’ll notice there is a while loop at the bottom of our program that is facilitating our play again functionality. We’re going to take that and extend its capabilities by adding more logic to capture the state of our previous game, and save that to display later.

When a game is complete, either through a win or a loss, capture the information we want and store it in an object. (for example, you could store whether it was a win/loss, the previous guesses, the amount of guesses it took to find the answer, etc.)
Once that is complete, use a constructor function OR class to create an object each time the game runs to completion. Each time you make a new object, store it inside the array of pastGames
Diving Deeper
While this is now a fully functional application, we can do better by creating a UI to display our snowman in the browser. Try creating an interface using HTML and CSS that will represent our snowman game, then link the JavaScript you wrote previously to the page. The methods we used to display the progress in our game will not work quite as well in the browser, so you will have to look into DOM manipulation using vanilla JavsScript OR jQuery.

Instructions:
Create a UI that represents the state of your snowman game. It should include the gallows for your snowman, and the stick figure that will slowly be revealed as the game progresses. (Hint: There may be easy ways to hide and show things using jQuery)
Using a <script> tag, add the JavsScript previously wrote to the page you just created. You will have to determine where each of these functions will fit into the flow of your game in the browser, as now our game relies on interacting with DOM elements instead of just the command line.
Unfortunately, readlineSync will not work as well in the browser, so use prompt() instead to facilitate guesses made by the user.
