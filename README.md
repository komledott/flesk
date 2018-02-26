# flesk

_Created by Terje Rudi. To be used freely._

Formats one or many HTML definition lists to display it's groups of `dt`- and `dd`-elements in a fluid and responsive layout.

This class initially sets the `dl`(s) to have a css style of `display: flex`, and dynamically wraps a `div` around the groups of defintion terms and data.

There is also a built in method for formatting any elements inside the definition list, by setting class(es) og just plain css.

# h2 Example A

Just any <dl> to be reformatted

```javascript
var dlAny = new RWformatDefinitionList();
```

# h2 Example B

Just one specific <dl> to be formatted, and with specific style to the <dt> elements inside

```javascript
var dlById = new RWformatDefinitionList(document.getElementById('SomeDlsId'),'width: 11em;margin: 0 0.2em 1em 0;color: #ff6633;');
dlById.setSubElmAttrs('dt',{
	'class':'testClassA',
	'style': 'font-weight: bold'
});
```

# h2 Example C

Any `<dl>` to be formatted as long as they belong to a defined css class. Default style to the `<dt>`+`<dd>` groups inside, and elemens getting extra css afterwards

```javascript
var dlByClassName = new RWformatDefinitionList(document.getElementsByClassName('SomeDlsClassName'));
dlByClassName.setSubElmAttrs('dt',{
	'class':'testClassA',
	'style': 'font-weight: bold'
});
dlByClassName.setSubElmAttrs('dd',{
	'class':'testClassB',
	'style': 'margin-left: 1em;display: list-item;list-style-type: square;font-style: italic'
});
dlByClassName.setSubElmAttrs('div',{
	'className':'link-list'
});
```
