Plus Sign
<selector> + <selector> means apply the styles only to the  <selector> directly following the first <selector>.
	
```css
article+article {
	margin-top: 3rem;
    padding-top: 3rem;
    border-top: 1px solid #c5c5c5;
}
```
	
Why Use It?
* This is a good way of styling every selector except the first one. For example if you have a list of articles. Good for things like padding etc.
	
More generally <selector2> + <selector2> means selector2 is a `sibling` of <selector1>. Compare this to <selector1> > <selector2> which means selector2 is a `child` of <selector1>.


	