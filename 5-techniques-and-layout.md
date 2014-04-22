# Techniques and Layouts

There are a couple of common layouts that floats work really well for, let's explore them.

## Grids

```html
<html>
	<head>
		<link rel="stylesheet" type="text/css" href="reset.css" />
		<link rel="stylesheet" type="text/css" href="style.css" />
	</head>
	<body>
		<div id="gallery" class="clearfix">
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
			<img src="old-time-scooter-cat.jpg" />
		</div>
	</body>
</html>
```

```css
body {
	padding: 10px;
}
#gallery {
	border: 1px solid red;
	padding: 10px;
}
#gallery img {
	float:left;
	width: 200px;
	height: 200px;
	border: 1px solid black;
	margin: 10px;
}
.clearfix:after {
  content: "";
  display: table;
  clear: both;
}
```

![image](http://i.imgur.com/oXwTBQJ.jpg)