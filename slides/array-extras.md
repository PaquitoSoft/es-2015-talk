##  Array extras

__Array.from__ converts array-like objects into truly arrays

<pre>
	<code data-trim>
export function findEls(selector, container) {
	return Array.from((container || document).querySelectorAll(selector));
}

// Also (only in Firefox)
for (let el of (container || document).querySelectorAll(selector)) {
	console.log(el);
}
	</code>
</pre>
