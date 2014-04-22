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

CSS, you crazy. It's as if that parent div barely exists, or at least is certainly not containing the children `div`s.