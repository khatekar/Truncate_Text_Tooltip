# Truncate_Text_Tooltip
Truncate Text Based on length and show tooltip using Javascript and CSS


# Sample Text:

`<div>
  <p>This is a very big text which needs to be truncated. This is new text to append. And show full text on hover</p>
 </div>`

`
div.p {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
`
The above snippet shows the text truncated using overflow property.


# Output

`<div>
  <p>This is a very big text which needs to be ...</p>
 </div>`


# Tooltip using css

`<div data-title="This is a very big text which needs to be truncated. This is new text to append. And show full text on hover">
  <p>This is a very big text which needs to be truncated. This is new text to append. And show full text on hover</p>
 </div>`

Use following css snippet to create tooltip::

# Now let us write the CSS.
`
[data-title] {
	font-size: 18px;
	position: relative;
	cursor: help;
}
`

# Now let us write CSS for hover.

`
[data-title]:hover::before {
	content: attr(data-title);
	position: absolute;
	bottom: -46px;
	padding: 10px;
	background: #000;
	color: #fff;
	font-size: 14px;
	white-space: nowrap;
}
`

That’s it. You can see the complete text on hover with a simple CSS code.



Most of the cases you may need to handle the text dynamically. Based on the design you might need to truncate your text based on maximum character length.


You need to use a simple Javascript code and your job is done.

`"your sample string".substring(0, characterLength);`

# Done! That's it.
