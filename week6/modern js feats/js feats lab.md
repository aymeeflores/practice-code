Lab: Modern JavaScript Features
In this lab we are going to practice using the ES6 module system within our create-react-app environment. We will try installing and importing from an external npm package. We will also create our own ES6 module so that we can also try exporting values from custom modules.

Getting Started
In terminal, initialize a new create-react-app called "es6lab"
Using an External Package From npm
In this step we will be installing an npm package (named lodash) and using ES6 imports to include it in your project

In your terminal, cd to the root of your new create-react-app project

Visit npmjs.com and search for the package named lodash. Take a quick look at the documentation and installation instructions

Use the npm install --save lodash command to install lodash into your project

In your App.js file, use the ES6 import syntax to import lodash as a default

Visit the lodash documentation at lodash.com and research lodash’s cloneDeep() method. Create an object with a few key-value pairs in it, and try using the cloneDeep() method to copy the object

Creating Your Own ES6 Module
Now it’s time to create our own module! Here we will practice exporting from our own custom module, and importing values into our main App.js file. We will be making a toolbelt module for a construction business

Default Exports and Imports
Create a new file called toolbelt.js in the src/js directory of your project

Create an array of strings that contains all your favorite household tools, and use the export default syntax to make that value the default export of your module

In your App.js file, import the default export from your toolbelt.js module. You will have to choose a name for it when you import it. Try printing the value that you imported using console.log. Confirm that it is the same array of tool names that you exported from your module!

Don’t forget: when importing from your own custom module, you must put a ./ in front of the package name in your import statement. Otherwise, it will look for a node_module called ‘toolbelt’

Named Exports and Imports
In toolbelt.js:

Create a named function called construction(). All this function should do is console.log the string 'CLANG!'

Export this function as a named export

Create an object to describe the properties of your construction business. It should have key-value pairs for your business name, address, and phone number

Store this object in a variable called ‘business’ and export it as a named export

In App.js:

Augment your original ‘toolbelt’ import statement so that you are also importing the two named exports we just created

Try calling the construction() function to confirm that it was imported correctly. You should see 'CLANG!' printed to the console

Use console.log() to print the name 'business' import that you just imported. Confirm that it was imported correctly by viewing it printed in the console

Try using the import {<export name> as <new name>} syntax to rename the named imports to a different name

Try using destructuring on the 'business' object you imported, to concisely pull out the values into individual variables

Bonus: Importing All Named Exports
In App.js:

Momentarily comment out your toolbelt import statement

Write another import statement that uses the \* syntax to import all named imports from your toolbelt module and place them into a variable

Hint: use the import \* as <variable name> syntax to store all the named imports into a variable
