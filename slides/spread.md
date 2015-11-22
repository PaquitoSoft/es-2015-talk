## <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator" target="_blank">Spread operator</a>

* Use arrays values separately
* Turn NodeLists into real arrays (FTW)

<pre>
	<code data-trim>
function sum(a, b, c) {
	return a + b + c;
}
let args = [2, 5, 7];
// sum.apply(null, args);
sum(...args);

let spans = document.querySelectorAll('span');
spans.forEach((el) => console.log(el.tagName)); // ERROR
[...spans].forEach((el) => console.log(el.tagName)); // "SPAN", "SPAN",...
	</code>
</pre>
