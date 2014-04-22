# Diving Deeper

Floats are wonderful for simple layouts. Let's consider the following:

```html
<html>
	<head>
		<link rel="stylesheet" type="text/css" href="style.css" />
	</head>
	<body>
		<div id="header">
			This is the header
		</div>
		<div id="content">
			This is the main content area
		</div>
		<div id="sidebar">
			This is the sidebar
		</div>
	</body>
</html>	
```

In our `style.css` we put the following:

```css
div {
	background: red;
	margin: 5px;
	padding: 10px;
}
#header {
	width: 530px;
}
#content {
	float: left;
	width: 400px;
	height: 200px;
}
#sidebar {
	float: left;
	width: 100px;
	height: 200px;
}
```
This would produce the following:

![image](http://i.imgur.com/vLo5ITK.png)

The `#header` `div`, which is naturally `display:block` remains on its own line. Meanwhile, `#content` and `#sidebar` are both floated left, so they remain inline with each other.

As a reminder: why is `#header` 530px wide? We want it to be the same width as the two elements below it. The actual width that `#header` is taking up is 560px:

+ 530px `width` 
+ 5px `margin-left` 
+ 5px `margin-right` 
+ 10px `padding-left` 
+ 10px `padding-right`

So: 

+ 400px (`width` of `#content`) 
+ 5px (`margin-left` of `#content`) 
+ 10px (`padding-left` of `#content`) 
+ 10px (`padding-right` of `#content`) 
+ 5px (`margin-right` of `#content`)  
+ 5px (`margin-left` of `#sidebar`) 
+ 100px (`width` of `#content`) 
+ 10px (`padding-left` of `#sidebar`) 
+ 10px (`padding-right` of `#sidebar`)
+ 5px (`margin-right` of `#sidebar`)

![image](http://i.imgur.com/kIqtt3T.png)

Hashtag math.

## Adding a Footer

Let's add a footer! Easy peasy, right? So now our layout looks like this:

```html		
<div id="header">
	This is the header
</div>
<div id="content">
	This is the main content area
</div>
<div id="sidebar">
	This is the sidebar
</div>
<div id="footer">
	This is the footer
</div>
```
And we'll add the following to our CSS:

```css
#footer {
	width: 530px;
	background: orange;
}
```

![image](http://i.imgur.com/xzLqWGL.png)

![image](http://i.imgur.com/58l5u0Y.png)

Wait why? What? What happened here? I didn't float the `#footer` element, why is it doing... that? And here, boys and girls, is your intro to:

## Floats Are Tricky

Boy howdy are they. When you're not careful, floats will run away with your layout and your heart. But we have some tools to put this back in order.

## Clearing Floats

At some point, we have to be able to stay "I do not want this element to wrap around the floated elements". And we can. Here comes the `clear` property:

```css
#footer {
	width: 530px;
	background: orange;
	clear: both;
}
```

Now we have something a lot closer to what we're looking for.

![image](http://i.imgur.com/uVKDWno.png)

## Bonus Round

To sidetrack for a moment, let's clean up our CSS a bit. You always want to strive to write the most concise code, within reason. So going back to our current CSS:

```css
div {
	background: red;
	margin: 5px;
	padding: 10px;
}
#header {
	width: 530px;
}
#content {
	float: left;
	width: 400px;
	height: 200px;
}
#sidebar {
	float: left;
	width: 100px;
	height: 200px;
}
#footer {
	width: 530px;
	background: orange;
	clear: both;
}
```

This is fairly verbose, and for our small page is totally fine. But consider this:

```css
div {
	background: red;
	margin: 5px;
	padding: 10px;
}
#header, #footer {
	width: 530px;
}
#content, #sidebar {
	float: left;
	height: 200px;
}
#content {
	width: 400px;
}
#sidebar {
	width: 100px;
}
#footer {
	background: orange;
	clear: both;
}
```

By combining selectors with common `properties` and `values`, we can change the values in one place. Want to change the width of `#sidebar` and `#content`? The `float`? You can now do it in one place instead of two.