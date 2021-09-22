Codealong: JSX
Introduction to JSX
JSX as the name suggests is a syntax extension to the JavaScript language with features that allow you to adapt JavaScript to React and its component-based architecture.

JSX is not a mandatory extension for React projects. However, using JSX will help you visually organize your React projects into components that have both the logic and the markup needed to work on a web page.

In the end, your browser does not understand JSX syntax natively and a transcompiler is needed. An example of one such transcompiler is Babel which can be installed in your React project to convert the JSX syntax into traditional JS syntax. If you are using create-react-app, Babel is already pre-installed so you can use JSX without any additional setup required.

A very simple JSX expression or statement would appear as follows:

const bigHeading = <h1>JSX is fun to work with!</h1>;

In the above statement, we aren't creating a string with an h1 tag, and neither is it plain HTML code. Rather, it is a JavaScript file containing exactly the markup needed for a simple component with an h1 tag inside of it. We have also assigned it to a constant variable. You can add that line of code and save the file with .js extension.

Because JSX is technically just a syntax extension to JavaScript, all of the code that you would otherwise write in a JavaScript file is still valid. For example, we can use values from a variable inside of HTML markup or a tag. We can then ask ReactDOM to render our markup stored inside of a JavaScript variable. Even though JSX might initially feel odd to use, it is very intuitive once you have written a component or two with JSX syntax.

To include any JS expression in JSX, we need to wrap it in curly braces, ie: {}

We can create comments in JSX by wrapping our comments in curly-braces and JavaScript's forward-slash and asterisk syntax like this:

{_/ Comments go here! _/}

JSX can include logical JavaScript expressions & operations as well. Let's look at an example that includes all of the basic JSX features and dissect the code line by line to understand JSX better.

First We are going to create a file called DisplayGrades.js and include the following code:

DisplayGrades.js Component
const students = [
{
studentId: 1,
firstName: 'John',
lastName: 'Doe',
grade: 75
},
{
studentId: 2,
firstName: 'Adam',
lastName: 'Smith',
grade: 90
}
];

const renderGrades = (student) => {
return (
<li key={student.studentId} className="list__item">
{student.firstName} {student.lastName} scored {student.grade}%
</li>
);
};

export default function DisplayGrades() {
const formattedGrades = students.map((student) => renderGrades(student));
return <ul className="list">{formattedGrades}</ul>;
}
Let's talk about what's going on in each line of code!

First, we create an array of student objects with a firstName, lastName and grade. Do pay attention to the naming convention here. As we are technically still writing JavaScript code, we will use camelCase.

Now, let's take a look at the DisplayGrades functional component. As a general best practice, please note that all React components should be named using PascalCase. The first line of code in our DisplayGrades component is mapping through the students array and then passes each student as an argument to a function called renderGrades. Pay attention to the fact that renderGrades is a normal JavaScript function outside of our DisplayGrades functional component, and we are just calling it inside DisplayGrades.

The purpose of the renderGrades function is to take the student passed to it as an argument and create a li tag with it. The content of the li tag includes the first name, last name, and grade associated with the student. We use curly braces around these values (e.g. {student.firstName}) to indicate that it's a value coming from a JavaScript variable and not just a string. You can see scored is not wrapped with curly braces as it is just a normal string that is not coming from a JavaScript variable. The same can be said for the % sign.

To summarize, we take the student object passed to the renderGrades function and create an li tag from it, then return it from the function back to where it was called from. In this case, the map function in the DisplayGrades component.

The map function will pass each student object to renderGrades and in the end, an array of li tags will be returned by the map function for each student. We now store this array of li tags in a variable called formattedGrades.

Because formattedGrades is a variable, we wrap it with curly braces {} and add it as content inside of ul tag and return it.

Note that we have added a key property to the li element in our return statement. When a component is rendered from an iterator such as map, a key property is needed to let React know which items have changed, are added, or removed. The key property should be something that uniquely identifies an item from it's siblings. If no unique property is available, the index of the item may be used, but this is not ideal. In this case, we use the unique property of each objects' studentId.

In addition, pay attention to how we add CSS class names in JSX files. Usually we would use the class keyword to attach a CSS class to a HTML element. But now, as we write this HTML component with JSX syntax, which is nothing but extended syntax of JavaScript, we can't use the class keyword as it is a reserved keyword in JavaScript. Instead we use className as a substitute.

Lastly, we can call this component from our index.js or any other React Component and render it in the browser.

import ReactDOM from 'react-dom';
import DisplayGrades from './DisplayGrades';

ReactDOM.render(<DisplayGrades />, document.getElementById('root'));
Our resulting HTML in the browser should appear as follows:

<div id="root">
  <ul class="list">
    <li class="list__item">John Doe scored 75%</li>
    <li class="list__item">Adam Smith scored 90%</li>
  </ul>
</div>
We can also import components located in different files into other components. Let's create a new header component in a file called Header.js.

In Header.js let's build out a basic header component with a logo.

Header.js Component
export default function Header() {
return (
<div className="main-header">
<h1 className="main-header__logo">LOGO GOES HERE</h1>
</div>
);
}
Take note that if we return multiple lines of JSX in our return statement, those lines must be wrapped in ().
return (

  <div className="main-header">
    <h1 className="main-header__logo">LOGO GOES HERE</h1>
  </div>
)
Let's take a moment to organize ourselves a little. We are going to create two new folders - components and pages.

Next, let's move our Header.js and 'DisplayGrades.jscomponents into ourcomponents` folder. If you're still running your app, you may get an error if you choose not to automatically update your import statements but that's ok - we'll fix that in just a second!

Now in our pages folder let's create a new file called Home.js.

Then in Home.js we will import our Header and DisplayGrades components at the top of the file and include the components in the return statement.

Home.js
import Header from '../components/Header';
import DisplayGrades from '../components/DisplayGrades';

export default function Home() {
return (
<>
<Header />
<DisplayGrades />
</>
);
};
Note that when we include our components in the return statement of our Home component we use a self-closing tag for the components <Header /> and <DisplayGrades />.

It is also important to note that all elements require a single parent element. Instead of using a div we can use a fragment to group a list of children without adding extra nodes to the DOM. Fragments can be rendered as <React.Fragment> </React.Fragment> or <> </> depending on the React version. Try rendering the <Header /> and <DisplayGrades /> components without the fragment and take note of the error that occurs.

We now have our two components rendering in our Home.js but we are still only rendering our DisplayGrades component to the DOM. Let's fix that by importing our Home.js into our index.js file and replacing <DisplayGrades /> with <Home />.

Your index.js should now look like this:

index.js
import ReactDOM from 'react-dom';
import Home from './pages/Home';

ReactDOM.render(<Home />, document.getElementById('root'));
Both our components should now be displayed on the page!

We can import all kinds of files - including images. Let's add a logo img to our header component to replace the h1 element.

First we import our image and give it name. In this case we are calling the img Logo.

Once the image is imported we can then use it with our src attribute by including it in-between a set of curly braces like so: {Logo}.

Our Header component should now look like this:

Header.js
import logo from '../assets/logo.svg';

export default function Header() {
return (
<div className="main-header">
<img src={logo} alt="school house logo" className="main-header__logo" />
</div>
);
};
Nice work! But the image for our logo looks a little too big. Let's fix that!

To use Sass within React we can run npm install sass in the root folder of our project. This will allow us to import and use our scss files directly into our Header.js file.

Next we will create a new scss file titled Header.scss and add the following styles.

Header.scss
.main-header {
padding: 1rem;
background-color: navy;
}

.main-header\_\_logo {
height: 50px;
width: 50px;
}
Once the file is created, we can import Header.scss into our Header.js file like so:
Header.js
import logo from '../assets/logo.svg';
import './Header.scss';

export default function Header() {
return (
<div className="main-header">
<img src={Logo} alt="school house logo" className="main-header__logo" />
</div>
);
};
As soon as we save the file, the updates to our styling will take effect!

You can pretty much do everything in JSX that you would otherwise do in JavaScript file. For more understanding, please read through official React documentation.
