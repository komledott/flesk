# flesk

Created by Terje Rudi. To be used freely.


E X A M P L E   A - Just any <dl> to be reformatted

var dlAny = new RWformatDefinitionList();


E X A M P L E   B - Just one specific <dl> to be formatted, and with specific style to the <dt> elements inside

var dlById = new RWformatDefinitionList(document.getElementById('SomeDlsId'),'width: 11em;margin: 0 0.2em 1em 0;color: #ff6633;');
dlById.setSubElmAttrs('dt',{
	'class':'testClassA',
	'style': 'font-weight: bold'
});


E X A M P L E   C - Any <dl> to be formatted as long as they belong to the css class. Default style to the <dt>-</dt><dd>-groups inside, and elemens getting extra css afterwards

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
