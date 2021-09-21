Codealong: Chrome DevTools Console
Using Chrome DevTools for running JavaScript in the browser
Chrome Dev Tools comes with it's own JavaScript console, which allows you to write and execute JavaScript right in the browser. It can be accessed through Console tab of the DevTools.

Console Tab

Reminder: you can open Chrome DevTools with a shortcut: Ctrl + Shift + J on Windows and Command + Option + J on Mac.

We use Chrome DevTools in this course, but all browsers have a JavaScript console, and steps below should translate well to any modern browser of your choosing.

When you first open the Console you will be greeted with a prompt (that looks like a right angle bracket followed by a cursor):

Console Prompt

At this point you can enter JS code and execute it by pressing Enter. We can start with something simple, like adding two numbers together using a + operator:

Return Value

Even though this is a pretty simple operation, there are a couple of important concepts that we can learn from it right away.

First, JS is an interpreted language, meaning it doesn't require a compilation step to run; it runs directly in the browser.

Second, any JS expression will result in a return value. In our case the return value is 27, because that is the return value of our + operator expression. The output of the return value of the expression has this little arrow looking icon before it: <-

Let's try something different. Let's create a variable and output it's value:

undefined Return Value

Here you can see that after we create a variable in console it becomes available for future use (be mindful that if you refresh the browser, all your variables and function declarations get cleared). All we have to do is call our variable and we will see it returns the value we set inside of that variable back to us.

As you might have already noticed, all of your inputs and outputs stay in the console window. If you want to clear the console window you can either execute the clear() command or click on the clear icon at the top of console window:

Clear Window Icon

Console will keep the history of all your commands, so if you want to run some code from before, you can use Up and Down arrows on your keyboard to shuffle through command history.

So far we've been entering single line expressions, however, console allows you to write multi-line code, by using Shift + Enter to go to next line. You can use Space or Tab for indenting lines of code, just like you do in VS Code:

Function in Console

In the example above, we've declared a new function that returns the result of adding two numbers passed in as parameters. After function declaration it will be available for use in current session until you refresh the browser. We just immediately invoke that function with the arguments to get the result back.

So far we've been writing all our code in the console directly. Browser console is also useful for debugging code that you write in standalone JS files as part of your application.

To output something to console you can use a console.log(); function. It takes any amount of arguments separated by comma, i.e. console.log('First', 'Second', window); and outputs them in the browser console.

Open a demo.html file in the browser (preferably using Live Server) and take a look at the console, you'll see that we have 3 lines of output for each console.log in demo.js file:

console.log Output

Whenever there is an output in the console from external source, on the right side of the output, you'll see a link that consists of the name of the file and line code that made this output. Clicking on it will take you to that place in the file:

Jump to Line

This feature will come in handy in your development practice to understand where debugging output or errors come from. As we learn more about JS, you will learn more ways to debug your code, but console.log will always remain the most direct and granular way to output the state of your application and find where the code is broken.

As we learn more JS concepts in upcoming days, continue practicing writing your expressions in Console and get comfortable with console.log function.

Diving Deeper
Do research on console object methods other than log.
Experiment with all interface elements of the console tab to see what other functionality is available.
