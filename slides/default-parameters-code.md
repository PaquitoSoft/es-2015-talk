##  Default parameters code

<pre style="width: 100%;">
	<code data-trim>
trigger(eventName, data = {}) {
	let listeners = this.eventsRegistry[eventName] || [];

	for (let listener of listeners) {
		try {
			listener.call(this, data);
		} catch (e) {
			console.warn(`Error in event (${eventName}): ${e.message}`);
		}
	}
}
	</code>
</pre>