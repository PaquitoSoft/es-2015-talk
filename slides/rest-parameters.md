## <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters" target="_blank">Rest parameters</a>

* A true array _arguments_ object
* No more _arguments.slice()_

<pre>
	<code data-trim>
function sum(base, ...numbers) {
	result = base;
	numbers.forEach(num => {
		result += num:
	});
	return result;
}
let x = 10;
console.log(sum(x, 2, 4, 5, 8)); // 29

// OLD
var args = Array.prototype.slice.call(arguments);
	</code>
</pre>