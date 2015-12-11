##  Classes code - I

<pre style="width: 100%;">
	<code data-trim>
class BaseController {
	
	constructor(options = {}) {
		this.data = options.data;
		this.template = options.template;
		this.partials = options.partials;
		this.domEvents = options.domEvents;
		this.defaultNavigation = 
			(typeof options.defaultNavigation === 'undefined') ? 
				true : options.defaultNavigation;

		// https://developer.mozilla.org/en-US/docs/Web/API/DOMParser
		// http://caniuse.com/#feat=xml-serializer
		this.domParser = new DOMParser();
	}
...
	</code>
</pre>