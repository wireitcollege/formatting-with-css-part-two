# The Wonderful World of Floats

So now that we have positioning in our toolkit, there is another essential CSS layout tool we need to add: floats.

The easiest way to think about floats is to think about images in a magazine.

![image](http://i.imgur.com/FAWlqEV.png)

In this case, the image is "floated" to the left:

```html
<html>
	<head>
		<style type="text/css">
		img {
			float: left;
			margin-right: 10px;
		}
		</style>
	</head>
	<body>
		<img src="http://www.kittyconnection.com.au/files/images/Kittyscooter2.jpg" />
		<p>Bacon ipsum dolor sit amet deserunt kevin rump, pork chop qui in commodo consequat eu. Pig hamburger flank shank, in enim shankle. In meatloaf salami, do tenderloin et in leberkas pastrami pork belly elit. Nisi chuck brisket anim.</p>

		<p>Brisket minim magna sunt fugiat deserunt ball tip. Ex tri-tip tenderloin, turducken biltong anim cow shankle swine nulla. Pork short ribs doner pariatur, et irure incididunt turducken spare ribs do excepteur ea swine. Tempor fugiat tail drumstick meatball, cupidatat bacon adipisicing biltong enim. Short ribs frankfurter labore enim pig sunt ribeye flank leberkas eu dolor ullamco. Eiusmod minim kevin nulla filet mignon t-bone.</p>

		<p>Boudin prosciutto culpa, leberkas in landjaeger occaecat cupidatat meatball irure. Salami velit strip steak, occaecat ad sirloin sed chicken. Ea tri-tip magna ut shankle consequat meatloaf laborum jerky voluptate. Porchetta et id qui venison sirloin short ribs sed non shank reprehenderit minim ut pastrami.</p>
	</body>
</html>
```

All we did is add `float: left` to the `img` tag. (We also added a little margin on the right hand side to separate it from the text). This removes the image from the normal flow of the document and allows the text to wrap around it.

If we kept the HTML exactly the same and simply changed the CSS `float` property value to `right`, we'd get this:

![image](http://i.imgur.com/hB18MXO.png)