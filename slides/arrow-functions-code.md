##  Arrow functions code

<pre style="width: 92%;">
	<code data-trim>
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
				console.error('RouterEngine::navigate# Error navigating:', 
					navError);
				this.trigger(RouterEvents.navigationEnd);
				this.trigger(RouterEvents.navigationError, navError);
			});
		} catch (err) {
			...
	</code>
</pre>

<aside class="notes">
	Parenthesis are optional if function has only one parameter
</aside>