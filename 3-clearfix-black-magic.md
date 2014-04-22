# Clearfix, or: What Kind of Black Magic Is This

Here's some more `float` trickery. Let's put a couple of divs, floated `left` inside a parent div:

```css
#parent {
	border: 1px solid red;
}
#parent div {
	float:left;
	border: 1px solid black;
	width: 200px;
	height: 200px;
}
```

```html
<div id="parent">
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
</div>
```

![image](http://i.imgur.com/u6kQ3jg.png)

CSS, you crazy. It's as if that parent div barely exists, or at least is certainly not containing the children divs. This is a very common problem when using floats, called the _collapse_ problem.

Basically, because all of the `#parent` children divs have been removed from the natural flow of the document, the `#parent` has trouble calculating its own height. Thankfully, we can help the browser out a bit. 

The `clearfix` hack has been around for some time, and has gotten simpler and simpler every year. Simply add this class to your stylesheet:

```css
.clearfix:after {
  content: "";
  display: table;
  clear: both;
}
```

And add the `.clearfix` class to any collapsed parent:

```html
<div id="parent" class="clearfix">
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
	<div>Floating so hard right now</div>
</div>
```

And looky-loo, we've fixed the problem:

![image](http://i.imgur.com/Uvu2f0k.png)