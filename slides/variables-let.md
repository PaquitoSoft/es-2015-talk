##  Variables let

<pre>
	<code data-trim>
configureEvents() {
	for (let key in this.domEvents) {
		let tokens = key.split('|');
		dom.addEvent(
			this.$el,
			tokens[0], 
			tokens[1] || undefined,
			this[this.domEvents[key]].bind(this)
		);
	}

	if (this.defaultNavigation) {
		dom.addEvent(this.$el, 'click', 'a', this.navTo);
	}
}		
	</code>
</pre>
