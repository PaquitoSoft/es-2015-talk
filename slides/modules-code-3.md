##  Modules code - III

<pre style="width: 100%;">
	<code data-trim style="max-height: 530px;">
// plugins/router.js
export let RouterEvents = Object.freeze({
	navigationStart: 'navigationStart',
	navigationEnd: 'navigationEnd',
	navigationError: 'navigationError',
	routeNotFound: 'routeNotFound'
});

export class RouterEngine extends EventsEmitter {
	static navTo(path, state = {}) {
		window.history.pushState(state, '', `#${path}`);
		window.dispatchEvent(new PopStateEvent('popstate', { state }));
	}
	...
}

// controllers/base-controller.js
import { RouterEngine } from '../plugins/router';

navTo(event, $target) {
	event.preventDefault();
	RouterEngine.navTo($target.getAttribute('href'));
}
	</code>
</pre>