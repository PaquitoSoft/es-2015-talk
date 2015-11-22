##  Proxies code - II

<pre style="position: relative; top: -15px; line-height: 23px;">
	<code style="max-height: 575px;" data-trim>
function Observable(target) {
	let observableRegistry = [];

	let proxy = new Proxy(target, {
		set: function(object, property, value, proxy) {
			let previousValue = object[property];
			object[property] = value;
			if (['onPropertyChanged', 'triggerPropertyChanged'].indexOf(property) === -1) {
				proxy.triggerPropertyChanged(property, previousValue, value);
			}
			return true;
		}
	});	

	proxy.onPropertyChanged = function(callback) {
		observableRegistry.push(callback);
	},

	proxy.triggerPropertyChanged = function(property, previousValue, newValue) {
		observableRegistry.forEach(callback => {
			callback.call(null, property, previousValue, newValue);
		});
	}

	return proxy;
}
	</code>
</pre>