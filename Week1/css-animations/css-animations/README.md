## Part 1

## Part 2 - CSS Animation Demo: Staff Dance Party

[Live demo](https://cssanimationdancingstaff.ernieatwyncode.repl.co/)

### Milestones

- [ ] Create a CSS animation so that the <h1> tag has a pulse-like animation that we'll call `pulse`.
- [ ] Set it up so when we hover over a staff member, their name expands by 30%. We'll do that by using the CSS `transition` property and the `transform` property.
- [ ] When we hover over the staff member, the image should also get brighter by 30% (using the `filter` CSS property) and create a silver box shadow of 150 pixels.
- [ ] Oh, and that image should also "dance" for us. We'll have to define what that means more specifically. The image should continue dancing until we move off the image.

### NOTE

> Transitions can’t change CSS properties. You set the property values on a selector and perhaps the selector’s `:hover` state. The transition defines how the change occurs, but not the specific start and end values.

> Animations, on the other hand, can change property values inside their keyframes. The property values don’t even need to exist outside of the animation keyframes. This makes animation far more dynamic and flexible than transitions. Also, transitions can't loop.

- [Via](https://www.peachpit.com/articles/article.aspx?p=2300569&seqNum=2)
