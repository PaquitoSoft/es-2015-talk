##  Modules code - I

<pre style="width: 100%;">
	<code data-trim>
// plugins/dom.js
function matches($el, selector) {
	let _matches = $el.matches || $el.msMatchesSelector;
	return _matches.call($el, selector);
}

export function findEl(selector, container) {
	return (container || document).querySelector(selector);
}

// controllers/home-controller.js
import * as dom from '../plugins/dom';

update() {
	let $updatedEl = this.render(),
		$prevPodcasts = dom.findEl('.podcasts', this.$el);

	dom.findEl('.badge', this.$el).innerHTML = this.data.podcasts.length;
	$prevPodcasts.parentNode.replaceChild(
		dom.findEl('.podcasts', $updatedEl),
		$prevPodcasts
	);
}
	</code>
</pre>