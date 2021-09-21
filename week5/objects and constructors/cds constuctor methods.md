Codealong: Constructor Methods
Introduction
In this exercise, you'll practice what you've learned about constructors and Object-Oriented Programming (OOP) by creating a small journal application. While similar to the object-oriented programming exercise in the JavaScript chapter, this exercise has a few nuances.

Instructions
Create a JavaScript file for this challenge. Inside this file, create constructor functions for two different types of objects - Journal and Entry. A journal is a collection of entries, just like a blog is made up of a collection of blog posts.

Each type of object is described below.

Entry
Each entry object represents one entry in the journal.

Each entry object should have the following properties:

title: Title of the journal entry
content: Content of the journal entry
author: Author of the journal entry,
likes: Number of likes that the post has
The likes property should begin at zero
Each entry object should have the following methods:

displayEntry() - When called on an entry object, prints that entry to the console with nice string formatting.
addLike() - When called on an entry object, increments the likes property of that entry
Journal
Each journal object must have the following properties:

name: The name of the journal
entries: An array of Entry objects. Must have zero items inside in the beginning.
Each journal object must have the following methods:

addEntry() - When called, this function:
Takes three parameters: title, content, and author
Uses the Entry constructor to create an entry object with the three parameters
Pushes the entry object into the entries array property
displayEntries() - Prints out all journal entries in the entries array property
deleteEntry(index) - Uses splice to remove an entry from the entries array. It should take in an index parameter indicating which entry to splice out.
Before you get started, think about what kind of objects you want to create, and what those objects are responsible for.
Diving Deeper
Once the the appropriate functions have been created and you can add and display your journal entries in the console, create a user interface (UI) for your journal using HTML, CSS, and JavaScript. You should be able to view and manipulate the journal from your browser instead of using the console.

This UI should include:

A form that allows the author to add a new journal entry
It should have form inputs for title, author and content
It should have a submit button for the user to submit their new entry
A section that displays all the blog posts that are in the journal (bonus: display them in reverse chronological order with the newest at the top)
When a user inputs the info for a new journal entry into the UI and presses submit, the new journal entry should be added to the journal and shown on the page.

Note: You should alter your displayEntry() function for the Entry objects so that instead of printing the entries to the console, it uses DOM manipulation to show them on the page.
