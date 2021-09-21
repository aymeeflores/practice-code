Codealong: CSS Chrome Inspector
Instructions
Open the included coffee-shop index.html file in a web-browser.
To open Chrome Dev Tools, click on the Chrome kebab menu, select More Tools then Developer Tools. Alternatively, you can use a shortcut, on macOS - Option + Command + I, on Windows - F12 or Control + Shift + I.
To open dev-tools with a DOM element pre-selected, right-click the element on the page and select Inspect
Due to the tool nature of Chrome Dev Tools, the following Codealong will focus on highlighting major functionality with some suggested exercises. It is also a good idea to spend some time and experiment with the tool on your own to get a feel for the useful features it provides.

Chrome Dev Tools has the following main sections illustrated in the screenshot below. The following description items correspond to the section numbers presented in the screenshot.

Section 1
Selection - allows you to select a DOM element on the page using a cursor. Elements will highlight as you hover over them with additional information provided.

There is color-coding in place with blue being the element’s content-box, green the element’s paddings and orange being the element’s margins.

Exercise: Spend some time hovering over different elements on the demo page to see different types of data the tooltip provides for different elements.

Section 2
Responsive Mode - allows you to emulate devices (such as mobile-phones and tablets) as well as set virtual device viewport settings (such as testing your design with 4K resolution on 13” screen). This feature will also show and let you select all current media-query breakpoints set on the site.

Exercise: Play around with different screen resolutions and device settings to get a feel for this functionality and how current designs reflect in screen and device changes. Try going to a variety of your favorite sites and do the same with them.

Section 3
DOM tree - this section represents the HTML structure of your page. The triangle icons on the left of each element allow you to expand/collapse nested HTML elements and also allow you to update HTML (content and attribute values).

Exercise: Spend some time expanding and collapsing HTML elements of the demo page. Notice that hovering over an HTML element will highlight it on the page as well as provide you with the element's dimensions. If you double click on the element, element attribute, or element text-content, you can edit the current values and the changes you make will be reflected after clicking off of the element. Right clicking on the element will allow you to do the following:

Add a new attribute or edit existing an one
Edit elements as HTML (which also allows you to add new HTML)
Expand and collapse all nested elements within the current element
Many other features, (take time to investigate all of them)!
Section 4
Styles Tab - this section will show all styles associated with the currently selected element in cascading order. This is a good tool for checking all the styles applied to the element, ordered by specificity as well as for troubleshooting specificity issues that might cause certain styles to be overridden.

Exercise: Take some time to inspect different elements on the page and look at their CSS cascade and inheritance. Please note that you can change property types and values by clicking on their respective, and also add new CSS properties by clicking on white space anywhere in the CSS declaration:

You can also click on the top-right corner text (eg: main.css:144) to navigate to the definition of that style in the linked CSS file. If you hover over a kebab menu in the bottom right corner of the style-declaration, you will see several UI elements that help you add text-shadows, box-shadows, text-color and background-color using wizards:

You can also add new inline element-properties and values in the element.style section:

You can filter out properties using the filter functionality:

You can also add new CSS classes and CSS class-styles (using the + button):

If you need to test out pseudo-classes (eg: :hover, : focus, :active), you can toggle element-state using the :hov button:

Section 5
Box Model - this section shows the currently selected element’s box-model. Going from inside outward it’s made up of content (blue), padding (green), border (yellow), and margin (orange). For values that are set, they are displayed in pixel-values respective to the direction (top, right, bottom left).

Exercise: Select some elements and try changing their values (eg: border-size, margin-top, padding-left, width). Notice how the changes are reflected in the box-model UI.

Section 6
Computed - shows all currently applied CSS properties for a selected element in alphabetical order. The UI will also allow you to expand and collapse each property by clicking a triangle icon. Expanding a property will provide an inheritance tree:

Filter input works same as section 4, returning all properties that has current filter query in their name:

Show all toggling will display all CSS properties, greying out the ones that are not currently applied. It could be useful for educational and exploratory purposes to get an idea of available properties.

Exercise: Change some element properties in section 4 and note how the changes are reflected in the computed properties if you add inline values or a new class, override existing properties, or change properties down the inheritance tree.

Please note that when the dev tools panel gets too small, the box model and computed sections get moved to a separate tab:

Section 7
Settings and More Tools - additional features can be found in this menu, many of which are more advanced. You can also control the position of the Dev Tools panel with the following options: detached, left side of the screen, bottom of the screen, right side of the screen.

Exercise: Go through available options in the menu and investigate the functionality it provides.

Additional Info
To explore Chrome Dev Tools more in-depth, check out Google's developer resources here.
