Method Chaining
Method Chaining in javaScript is a technique used to pass values along a chain of functions. In order to understand method chaining, we will first investigate the use of return statements followed by the proper syntax.

Expressions, Statements and Functions
A small fragment of code that produces a value is called an expression. Very loosely, you can think of it as a word, a term or a sub-sentence in English. Continuing on with this analogy, a statement can be thought of as a full sentence.

1;
// the code above is a statement consisting of one expression. Just like how a sentence in human language can be composed of one term. "Hey!"
If a nested collection of expressions is a statement, you can think of functions as a collection of statements. A function is a small program wrapped in a value, as in they are lines of code deliberately intertwined together to perform a specific "function".

function difference(x,y) {
var minus = x - y;
if (minus < 0) {
minus = -minus
};
return minus;
}
// a collection of statements are wrapped in a function named "difference"
Returned Values
All expressions, statements, and functions return a value. From a high-level perspective, you can think of it as always receiving an output given from the "computer" (or browser or JavaScript interpreter) for any of your input.

In your chrome console, try typing the following line by line:

1;
console.log(1);
For the first line 1; you will see that as you press enter, it displays another line right beneath it.

When you try the second line console.log(1) you will notice that you get two new lines after you press enter. The first line shows 1 and the second one shows undefined. The function console.log() prints the value you put in to the corresponding console (in this case, our browser console), but ultimately it returns an empty value undefined. Understanding the difference between what a statement or a function returns as its value, and what they do while reaching that point is important.

The ++ operator will increment a numeric value by 1. So if we do var x = 1; x++;, x will now be 2. ++x; will increment x by 1 the same way. However, this is what the operators do "on the side." Their explicit return value when used in a statement are different. One returns the value before the increment, the other will return the value after the increment. Try out the following code in your console:

var x = 1;
var y = x++;
var z = ++x;
x;
y;
z;
Using Returned Values
Understanding how statements and functions always return a value (it could be an "empty" value like undefined) is important, because many functions are written to have other functions nested inside and use their returned value. As an example, let's revisit the difference() function we showed you earlier.

function difference(x,y) {
var minus = x - y;
if (minus < 0) {
minus = -minus
};
return minus;
}
It takes in two parameters, subtracts one from the other, then see if the returned value is positive. If negative, it multiplies it by -1, then returns that value at the end. Now, consider the following code.

function difference(x,y) {
var minus = x - y;
if (minus < 0) {
minus = -minus
};
return minus;
}

function bigDifference(x,y) {
if (difference(x,y) > 100) {
console.log("Yes the difference is big!");
} else {
console.log("No the difference is small");
}
}
Inside the function bigDifference(), you will find the function difference() being used. When that particular line is read, difference() will be executed with the parameters given into to bigDifference(). As it explicitly returns a certain value, that value will be used in evaluating the if statement. For example, if x was 40 and y was 8, difference(x,y) will return 32, and the if statement will be evaluated like so: if (32 > 100)

Method Chaining
Method chaining is a technique that is used often in JavaScript. For example, you might run into situations in which multiple functions are being called on the same object consecutively. Chaining your functions may provide you with means to simplify your code.

It is usually easier to see with JQuery. Let's consider the following jQuery code:

// capture a <table> element in HTML and store it in a variable
var table = $('table');
// append a jQuery <tr> element inside the <table> and store it in a different variable
var tr = table.append($('<tr>'));
// append a jQuery <td> element inside the <tr> and store in in a different variable
var td = tr.append($('<td>'));
// insert some text inside the table data
td.text('Hello');
First, we're using jQuery to capture a

element. This jQuery object has the method .append(), in which you can insert a jQuery object as a parameter and it would be appended inside the
. This method returns the inserted jQuery object. This is why we can store that returned object inside another variable called tr. We then follow a similar process to create another jQuery object for object, and have it stored in a variable called td. Finally, we are using the .text() method onto td to put some text inside.
Without the understanding of how functions can return values and how those values can be used (e.g., saved in a variable), the above code may not have made much sense. But we can do even better. Consider the following code:

// chain methods one after another without saving the midpoints in variables
$('table').append($('<tr>')).append($('<td>')).text('Hello');
Now that we understand that table.append($('<tr>')) would return $('<tr>'), we can call the method .append() right behind it.

Chaining methods is not always superior. It makes it more efficient by condensing code, but it may make your code harder to read. As a rule of thumb for now, chain methods up to a point where it makes it easier for yourself to read.

In a nut shell, this form of writing JavaScript is largely designed to reduce the number of lines of code you write. By using method chaining, you only have to reference the element (in the case above $('table')) you are performing the actions on once.

Summary
Method chaining is about reducing redundancies in your code. However, it has a more powerful use with something called Promises. Promises will be investigated in more detail with React and AJAX, but if you are curious, feel free to investigate the .then() method in JQuery.

, append it inside the jQuery
