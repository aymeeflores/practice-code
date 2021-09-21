Codealong: Media Queries
This codealong will introduce you to using Media Queries.

Before you begin, ensure you have the Live Server extension installed, and SASS installed and configured in VSCode. With the index.html selected, click "Go Live" to start your server. Also be sure to start compiling your SASS.

Please download the starter code here.

Instructions
It's always a good idea to familiarize yourself with any codebase before making changes, so take a minute to look through each of the files in this codealong.

Once you're familiar with each of the files in this codealong, open the index.html in your browser. You should see a column of lightblue boxes in your gallery, with each box taking up a single row.

Try resizing your browser window. No matter how wide the window is, each box takes up one whole row. This is great for mobile, but on wider screens it makes more sense to take advantage of the extra screen real estate and show a little more content. Let's leverage the power of Media Queries to do just this!

Take a look at \_mixins.scss. What's going on in there?

We've defined two mixins called tablet and desktop using the @mixin at-rule. (Remember, to invoke or use a mixin later on, we use the @include at-rule.)
Inside each mixin, we're using the @media at-rule to define a media query for the tablet and desktop breakpoints.
Inside each media query, we're using the @content at-rule to inject any styles passed to the mixin inside curly braces {} when it is invoked. For more information on the @content at-rule, please see the SASS documentation here.
What this means is that anywhere we want to define styles that apply specifically for tablet screen sizes, all we have to do is:

@include tablet {
// tablet-specific styles go here
}
Once the condition of the media query is met (in this case, min-width: $tablet-breakpoint), any styles between the curly braces after @include tablet will be applied.

Now that we understand these mixins and how to use them, let's put them to work!

Using the tablet mixin, apply the following styles in main.scss:
@include tablet {
.gallery {
flex-direction: row;
flex-wrap: wrap;
justify-content: space-evenly;
align-content: space-evenly;
&\_\_item {
width: 40%;
margin: 3vw 0;
background: lightgreen;
}
}
}
Save your changes, then go back to your web browser. Try resizing the window from the smallest width to the largest width you can. You should now see that when the window is wider than 768px, each row in your gallery holds up to two boxes, and each box is now lightgreen!

Let's extend this further and apply some desktop-specific styles now. Using the desktop mixin, apply the following styles in main.scss:

@include desktop {
.gallery {
&\_\_item {
width: 30%;
margin: 1.25vw 0;
background: lightpink;
}
}
}
Save your changes, then go back to your web browser. Try resizing the window from the smallest width to the largest width you can. You should now see that when the window is wider than 1280px, each row in your gallery holds up to three boxes, and each box is now lightpink!
Since we're using SASS, we can also nest media queries inside of other selectors. This is preferred over having one big chunk of CSS for all of our tablet and desktop styles.

Let's refactor our code to nest our responsive styles directly inside of the appropriate selectors. Using the the tablet and desktop mixins, apply the styles inside of the .gallery and .gallery\_\_item selectors:
.gallery {
...

    @include tablet {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-evenly;
        align-content: space-evenly;
    }

    &__item {
        ...

        @include tablet {
            width: 40%;
            margin: 3vw 0;
            background: lightgreen;
        }

        @include desktop {
            width: 30%;
            margin: 1.25vw 0;
            background: lightpink;
        }
    }

}
