##  Default parameters code

<pre>
	<code data-trim>
trigger(eventName, data = {}) {
	let listeners = this.eventsRegistry[eventName] || [];

	for (let listener of listeners) {
		try {
			listener.call(this, data);
		} catch (e) {
			console.warn(`Error triggering event with name ${eventName}: ${e.message}`);
		}
	}
}
	</code>
</pre>