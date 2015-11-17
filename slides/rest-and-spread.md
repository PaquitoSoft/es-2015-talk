##  Rest parameters and Spread operator

* A true array _arguments_ object
* Use array values separately

<pre>
	<code data-trim>
function sum(base, ...numbers) {
	result = base;
	numbers.forEach(num => {
		result += num:
	});
	return result;
}
let x = 10,
	others = [2,4,5,8];
console.log(sum(x, ...others)); // 29
	</code>
</pre>