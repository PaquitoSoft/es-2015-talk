##  Proxies code - II

<pre style="position: relative; top: -15px; left: -20px; line-height: 23px; width: 95%;">
	<code style="max-height: 575px;" data-trim>
function Observable(target) {
	let observableRegistry = [];

	function triggerPropertyChanged(property, previousValue, newValue) {
		observableRegistry.forEach(callback => {
			callback.call(null, property, previousValue, newValue);
		});
	}

	let proxy = new Proxy(target, {
		set: function(object, property, value, proxy) {
			let previousValue = object[property];
			object[property] = value;
			if ('onPropertyChanged' !== property) {
				triggerPropertyChanged(property, previousValue, value);
			}
			return true;
		}
	});	

	proxy.onPropertyChanged = function(callback) {
		observableRegistry.push(callback);
	};

	return proxy;
}
	</code>
</pre>