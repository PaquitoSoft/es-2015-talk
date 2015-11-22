## <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of" target="_blank">for...of</a>


* Allow iteration over new and old types: Map, Set and Array, arguments
* Iterates over values, not properties
* Promising iteration over NodeList (only Firefox right now)

<pre>
	<code data-trim>
let arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
	console.log(i); // logs "3", "5", "7", "foo"
}
for (let i of arr) {
	console.log(i); // logs "3", "5", "7"
}
	</code>
</pre>