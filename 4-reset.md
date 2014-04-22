# The CSS Reset

We've discussed how there are different layers of CSS that affect the styles that you are applying on the page, one of them being the default browser styles.

The tricky bit about the default browser styles is that they are all different. Chrome, Safari, Firefox, Internet Explorer... they all have a slightly different default stylesheet to contend with.

This becomes more important as we work with layouts, particularly floats. The browser defaults will cause unintended side effects that will get in the way of a consistent cross-browser display.

Fortunately, we do have a tool to combat these undesired side effects: The CSS Reset.

## What It Is

The CSS Reset essentially levels the playing field across the board, setting defaults for every element no matter the browser. There [isn't one reset to rule them all](https://www.google.com/search?q=css+reset), it really depends on what you're trying to accomplish.

A very basic reset is something like the following:

```css
* {
	margin: 0;
	padding: 0;
	border: 0;
}
```
What this means is that _everything_ (`*`) (every element in the DOM) should have no `margin`, no `padding`, and no `border`. These are common browser defaults that can get in the way of the layout you desire.

Now you can go ahead and override these `properties` for individual elements:

```css
body {
	padding: 10px;
}
#content {
	margin: 20px;
	border: 1px solid blue;
	font-size: 12px;
}
```
## Resources

You can check out some popular CSS Resets [here](http://www.cssreset.com/). It's generally considered good practice to keep your reset CSS in a separate stylesheet and just include it within your `head` tag first, before any other rules are defined.

```html
<link rel="stylesheet" type="text/css" href="reset.css" />
<link rel="stylesheet" type="text/css" href="style.css" />
```