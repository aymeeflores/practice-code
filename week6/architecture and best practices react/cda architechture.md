Codealong: React Architecture
Getting Started
There are multiple ways to structure your React applications, and quite often it is a matter of personal preference. However, as a beginner React developer you can benefit from having the experience of the developer community and some of the sane defaults that have been created. Later, as you gain more experience, you will start developing your own patterns that help operate as effectively as possible when working with React. In this codealong we will build a simple application that uses the concepts we have learned thus far.

For this exercise, please download the reference code here. You can use this reference code to compare it to the notes mentioned in the section below.

Notes
Use create-react-app to start a new application. It will give you a great starting point for development (hot reload, file importing, etc.), testing, and creating deployment versions of your application

There are many useful packages available for your use, so it is highly recommended to become familiar with the Node Package Manager (npm) ecosystem.

For this codealong, we want to use SASS which isn’t available right out of the box. In order to obtain this functionality, we must install it with npm i sass inside of your React application folder.

It’s always a great idea to have unique IDs for your data, so we will use the uniqid package for this codealong: npm i uniqid.

The starting point of the application is the index.js file. Notice that the App component is wrapped in React.StrictMode component that will help with catching possible bad practices in your code - [https://reactjs.org/docs/strict-mode.html](React.StrictMode documentation)

For this application we will be building a simple Dev Skills Roadmap tracker that will allow us to manage areas of improvement and goals for each of the technologies.

Keep your general SCSS (typography, variables, mixins, etc) in a separate folder (eg: styles) and import it in index.js.

Keep your file structure as following:

One component per file (Component.js)
Each component has it’s own folder (/Component)
Create and index.js file where you just export Component.js file (export { default } from ‘./Component;), this will allow you to have cleaner imports, ie: import Component from ‘components/Component and still keep the component name in the file name opened in your code editor
Components that do not have any state should be functional components, and stateful components should be class components. If you have event handlers local to the component, make it a class component as well. Essentially, functional components are display components. If your component only takes props and renders them, it’s likely that it needs to be a functional component. Default to functional components, and promote them to a class component when additional functionality is required.

Keep your state either local (only used for that component internally, not shared with other components), or keep shared state just high enough in the component tree where it can be passed down to other components via props. Be mindful that state is not too high that it causes unnecessary component re-renders, and not too deep where you would have to duplicate it.

Keep JSX props on a separate line, unless it’s a one-liner component.

Use destructuring in your component props to keep your code more concise.

Keep your CSS local to the components it belongs to. In the component folder, use BEM convention, remember to use className to define class names.

Be preferential towards using a declarative approach, and utilize the map and filter functions to render your JSX.

Remember to use the key attribute for any iterated content.

Use events, props handlers, and state for your forms. Avoid using ref functionality, and rather rely on onChange event, keep your data as a SSOT in state and pass that data via props to related elements. Be preferential towards using the handleEvent naming convention for your event handlers.

It’s always a good idea to validate your forms and there are libraries to help you with that. Even simple conditional validation added for empty fields and wrong data types goes a long way.

When you update React state, remember that it needs to be immutable, do not mutate React state directly, always use setState, favor spread syntax and immutable array and object methods to update your state.

Use && and tertiaries to render components and classes conditionally.

Use anonymous function callbacks to send data back to parent components via passed arguments in props handlers.
