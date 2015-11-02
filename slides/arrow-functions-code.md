##  Arrow functions code

<pre>
	<code style="max-height: 450px;">
processRoute(path, state = {}) {
	...
	if (routeConfig) {
		try {
			routeConfig.handler({
				url: _path,
				params: routeConfig.path.match(_path),
				state
			})
			.then(this.navigate.bind(this))
			.catch((navError) => {
				console.error('RouterEngine::navigate# Error navigating:', navError);
				this.trigger(RouterEvents.navigationEnd);
				this.trigger(RouterEvents.navigationError, navError);
			});
		} catch (err) {
			...
	</code>
</pre>