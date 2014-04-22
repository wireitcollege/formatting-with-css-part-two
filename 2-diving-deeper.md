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