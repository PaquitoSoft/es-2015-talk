## <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment" target="_blank">Destructuring</a>

* Pick selected properties from objects and arrays
* Allow for default values (if none, _undefined_ is the default)
* Very useful when _importing_ modules to allow **tree shaking** (ex: [Rollup.js](http://rollupjs.org/))

<pre>
	<code data-trim>
	// Router
	export let RouterEvents = {}
	export class RouterEngine extends EventsEmitter {}

	// BaseController
	import { RouterEngine } from '../plugins/router';

	// Arrays
	let arr = ['Rollo', 'Tomassi', 46];
	let [name, surname, age] = arr;
	</code>
</pre>
