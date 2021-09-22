Codealong: React Dev Tools
Instructions
Install React Developer Tools

To install the "React Developer Tools" Chrome extension go to this URL and click "Add to Chrome". This will prompt you with a message about the extension's permissions, click "Add extension" to confirm and finish installing.

Note that after installing you will get two new tabs in your Chrome DevTools: "⚛️ Components" and "⚛️ Profiler".
The Components tab shows you the root React components that were rendered on the page, as well as the subcomponents that they ended up rendering.
Load a React page (or the provided demo), in order to test the new dev-tool.

Open Chrome's Developer Tools and find the React Components Inspector. If you don't see something that says "⚛️ Components" try clicking on the >> symbol to see more tools.

Using the Components Inspector

Each component can be opened up to see the HTML returned from it's render method
Clicking on the arrow icon dev-tools arrow icon will allow you to select a component in the browser window which will show info about the component in the developer-tools window.
react components inspector

Inspecting Component Props

When you click on a component, using React Developer Tools, on the right of the tools panel you should see information related to the component such as the components props and state, if the component has props and state.

inspecting component props

Using searching to inspect a component:

searching components

Try interacting with your app, using React Developer Tools see if you can observe state changes and prop changes by editing your code e.g. using setState(). Once you feel more comfortable with the developer tool try inspecting other React sites such as the example sites listed at reactjs.org/community/examples
