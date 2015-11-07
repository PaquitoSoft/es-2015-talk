##  Template strings code

<pre>
	<code data-trim>
static navTo(path, state = {}) {
	window.history.pushState(state, '', `#${path}`);
	window.dispatchEvent(new PopStateEvent('popstate', { state }));
}

function foo() { return 42; }
console.log(`The meaning of life is: ${foo()}`);
	</code>
</pre>