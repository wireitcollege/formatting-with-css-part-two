# Fixed Positioning

So far we've explored a couple different values for the `position` property: `static`, `relative`, and `absolute`. There exists yet another `position` value: `fixed`.

Fixed positioning works in relation to the browser window, no questions asked. It doesn't matter what `position` value its parent element has, it aligns itself with the window, and it stays there.

```html
<html>
	<head>
		<link rel="stylesheet" type="text/css" href="style.css" />
	</head>
	<body>
		<div id="fixed-div"></div>
		<p>Bacon ipsum dolor sit amet pork belly sausage pork chop kielbasa landjaeger tenderloin.  Tenderloin jerky t-bone beef tongue prosciutto pig.  Leberkas porchetta ribeye tri-tip.  Tail pork chop pork leberkas.  Strip steak sirloin tri-tip bacon, ham sausage ball tip brisket.  Kevin fatback short ribs, ham hock meatloaf swine tongue biltong t-bone spare ribs andouille turkey turducken.  Biltong tenderloin doner, capicola bacon sausage corned beef leberkas chuck landjaeger jowl flank pork swine.</p>

		<p>Strip steak tail meatball pork chop porchetta.  Capicola pork loin short ribs shankle pork pork belly andouille filet mignon chuck doner venison hamburger beef kielbasa.  Tongue sirloin chicken corned beef meatloaf, sausage rump pastrami shankle andouille jowl capicola.  Swine leberkas turducken spare ribs, bacon pig doner ham hock pork jowl pastrami porchetta tongue chuck shoulder.  Andouille capicola tongue pork tri-tip cow biltong turkey boudin.</p>

		<p>Tenderloin andouille swine beef ribs.  Turkey rump beef ribeye pancetta shoulder landjaeger biltong turducken meatball beef ribs.  Pancetta prosciutto sirloin ham corned beef ribeye drumstick turducken frankfurter doner filet mignon strip steak.  Tri-tip ground round pork belly prosciutto jerky meatloaf, corned beef bacon.  Flank chuck turducken tongue kevin leberkas.</p>

		<p>Tri-tip chuck fatback venison rump prosciutto drumstick landjaeger bresaola strip steak frankfurter filet mignon pork chop boudin meatball.  Spare ribs biltong jerky, flank tongue short ribs pancetta kielbasa tri-tip shank ribeye bacon chicken andouille hamburger.  T-bone doner chicken kevin beef ribs shoulder pancetta.  Tongue ribeye strip steak pork belly short ribs jowl turkey pork chop shoulder bacon kielbasa corned beef hamburger tri-tip.</p>

		<p>Jerky shank prosciutto, short ribs ball tip pastrami salami pork pork belly tongue meatball bacon fatback doner filet mignon.  Boudin filet mignon chuck ham hock, fatback sirloin capicola bresaola bacon strip steak jowl spare ribs rump.  Turducken boudin capicola kevin, bresaola shank pork belly spare ribs ham hock pork chop hamburger pork loin porchetta swine.  Venison pork chop beef ribs, pork belly hamburger tongue pork beef.  Bacon ham prosciutto, shankle sirloin pork porchetta kielbasa rump shoulder.</p>
	</body>
</html>
```

```css
#fixed-div {
	width: 200px;
	height: 200px;
	background: red;
	position: fixed;
	top: 0;
	left: 0;
}
```

![image](http://i.imgur.com/mOlZMcN.png)

It doesn't matter where you scroll, or where `#fixed-div` resides within the DOM, it will always be in the upper left hand corner of the window.