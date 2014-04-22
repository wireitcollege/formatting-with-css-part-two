# Diving Deeper

The `float` property has four valid values: `left`, `right`, `none`, and `inherit`.

We've already covered `left`, and `none`, let's take a look at the other two.

## None

Sometimes you want to explicitly declare that the element in question should not `float` at all. Setting it to `none` will do the trick just fine. Barring the `position` property, this ensures that the element will fall within the natural flow of the document.

## Inherit

Setting `float: inherit` means that the element will take on the same `float` value as its parent element. For example:

```html
<div style="float:left;">
	<p style="float:inherit">This paragraph will also float left because the parent div floats left.</p>
</div>
```