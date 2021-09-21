# Demo: BEM

> "There are only two hard things in Computer Science: cache invalidation and naming things."
> -- Phil Karlton

## To Do

### Example 1: BBC's Home Page

### Example 2: Button Gallery

- [ ] Take a look at button-gallery.html BUT DON'T DISPLAY THE PAGE
  - What do you notice? What's the difference between the terms that separate `__` and `--`?
  - What do you think I would do to make a button big or small? Or change its color?
- [ ] Display the page. Is it what you expected?
- [ ] Now let's try this for the hummus page!
  - [ ] What are good candidates for BLOCKS?
  - [ ] What are good candidates for ELEMENTS within the block?
  - [ ] Are there any examples of MODIFIERS here?
    - [ ] If there isn't, let's make one!

### The good things about BEM

- BEM implies the same coding standards within dev teams. THIS IS THE #1 REASON WHY A LOT OF DEV TEAMS WILL USE BEM!
- There is independent development of each module.
- BEM is useful to fix CSS Inheritance & Specificity
- Uses only class selectors
- Keep specificity low by not having a nested selector
  the case for universal selectors can be ignored considering all the selectors being very unique
- Adding, removing, replacing a block of CSS is much easier as there is no tight coupling between HTML and CSS
- Easier to understand what CSS does just by reading class names in html
- Writing component specific CSS becomes much easier by not using HTML tag names in CSS; both HTML and CSS are decoupled. Changing the HTML tag to be something else will not affect CSS.
- Better performance as browser has to spend less time figuring out the nesting in CSS (which doesn't exist in BEM)
- No classname conflicts.

### The not so good things about BEM

- "I JUST learned about complex selectors and now you're telling me that everything should be 1 or 2 weird class names?" With BEM: Yes. Yes we are.
- Wow, that HTML looks... bloated and ugly. Users of websites care about fast loading websites, not how the source code looks behind the scene
- CSS file size will increase, although you can gzip and minify production code

## Resources

- [BEM Cheat Sheet](https://9elements.com/bem-cheat-sheet/)
