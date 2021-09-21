Lab: Web APIs and Axios
Getting Started
To get started, please download the starter code here.

In the starter you will find an HTML template that you will fill with content in JavaScript. Get the data from the web API using axios, and then select the elements using the DOM API, and insert the appropriate data.

Exercises
We’re going to be using the Req | Res REST API to make requests to the test API and get the real responses back. Spend some time going through available endpoints and the documentation for them, as well as sample requests.

Using starter code, that already includes the library, we will use axios to get the Response object that contains the data

Since axios returns a promise, use the .then() method to retrieve the data

This method accepts a function as an argument with a single parameter called "response"
This response object has a data property which contains all of the data you will need
Try console.logging the response object to see its contents
An example of what you could do to see the data is this:

const usersURL = ‘https://reqres.in/api/users?page=1’
axios.get(usersURL).then(response => {
console.log(response.data);
});
Now using the response data object, populate the HTML elements with the returned data:
Insert the data for page and total_pages from the response into res**page and res**total-pages span elements respectively

Populate the res-users list with all returned users from the data property of the response so it matches current HTML element structure but has dynamically generated elements

Make sure that you start with an empty user's list element before inserting new user list items

Make sure you set the res-users\_\_avatar element src attribute to match each user’s avatar response data property

Make sure the avatar is no larger than 50px in height

Populate the res\_\_ad spa element with the value returned in the support property of the response object:

What happens when you try to set the HTML of the element to complex data type?

Try using JSON.stringify to populate the span element with the text representation of the support object

How would you display that data as a code snippet?

Research pre and code HTML elements and how they can be used to display text content as code
Research lesser known third parameter of JSON.stringify that allows you to add indentation to string output
Try changing the URL of the endpoint to a different page query param value to see the content change dynamically
