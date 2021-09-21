Lab: Promises
Lab: Promises
Think about the process of buying something at a store with a credit card.

We tap or swipe our card at a credit card machine to pay for an item
The machine takes some time to connect to the company's database
If the credit card has enough credit, we can buy the item. In that case:
The price of the item is charged to our card, increasing its balance
We now own the item we purchased
The machine lets us know that the transaction was successful
If the credit card has reached its limit, we can't buy the item. In that case:
The machine lets us know that the transaction was declined
Checking our credit card statement afterwards would reveal the new balance on our credit card
png

This would work well as an asynchronous process because of step two: the machine takes some time to connect to the company's database. When we first swipe our card, the machine doesn't yet know whether or not we can afford an item, and it could take several seconds for it to find that out before completing the transaction. The machine promises that it will tell us if our transaction succeeded as soon as it finds out. Our credit card statement would only show a new balance if we check it after this process has finished.

Getting Started
We will use Promises to build the process described above.

Download the starter code here. You are provided with the following:

creditCard: Your credit card object, which will be used to buy products.
products: An array of the products you can buy.
displayBalances: This function displays the Credit Card Statement and Products You Own in the browser via the DOM. You can call it whenever you want to update the information on the screen.
buyProduct: This function returns a Promise. After a couple seconds, the promise resolves if the purchase is successful, or rejects if the purchase is unsuccessful. This is the function you will need to call in order to buy a product.
png

Part 1: Going Shopping
Call the buyProduct function to purchase a T-shirt. What does it return?

Once the promise resolves, then call displayBalances to show the updated credit card statement on the screen. Hint: use the .then() method to make sure you do this once the promise has resolved. You should see a balance of $20 on the page.
console.log the result of the promise, which is passed as a parameter to your .then() callback function. You should see an object with the string "Purchased T-shirt for $20" in your console.
After buying the T-shirt, buy a Handbag. To ensure this happens in the right order, remember that you can chain .then() methods by returning the next promise from your callback function.

Once the handbag is purchased, call displayBalances to show the updated credit card statement.
console.log the result of the promise.
Next, buy a Computer. As before, try displaying the updated credit card statement and console.log the result of the promise.

Uh oh! The promise rejected because you didn't have enough credit.
Your balance didn't update.
Check the console to see that there is an error for an uncaught promise rejection.
We need to handle this rejection using the .catch() method.

Add a catch function to your promise chain and make it console.log the error that occurred.
Now if any of our purchases are declined, the .catch() callback will run and handle the error. You should see an object with the string "Declined purchase of Computer for $2000" in your console.
Part 2: Promise.all
Instead of buying each product one after the other, let's buy them in parallel using Promise.all.

Use Promise.all() to buy three items at the same time by passing it an array of promises.
When all three purchases have succeeded:
Call displayBalances
Log "Purchased 3 products" to the console
You can use the .then() method to achieve this.
When any of the purchases are declined:
Call displayBalances
Log "Failed to purchase all 3 products" to the console
You can use the .catch() method to achieve this.
Diving Deeper: Refunding a credit card
So far, we have practiced consuming the promises which are produced by the buyProduct function. We can create our own promise-producing functions using the new Promise() constructor.

Your task is to write a function called refundProduct which:

Takes a product object as a parameter
Returns a Promise, which will:
Reject if we don't own that product
Resolve if we do own that product. Also add the price of the product back to creditCard, and subtract 1 from the numberPurchased of that product.
Hint: inspect the buyProduct function for inspiration, as your task is to make a function which does the opposite.

Test your refundProduct function by calling it within your Promise.all() from Part 2.
