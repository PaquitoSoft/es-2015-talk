##  for...of

* Allow iteration over new and old types: Map, Set and Array, arguments
* Iterates over values, not properties
* Promising iteration over NodeList (only Firefox right now)

<pre>
	<code data-trim>
let arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
   console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
   console.log(i); // logs "3", "5", "7"
}

// Note: This will only work in platforms that have
// implemented NodeList.prototype[Symbol.iterator]
let articleParagraphs = document.querySelectorAll("article > p");

for (let paragraph of articleParagraphs) {
  paragraph.classList.add("read");
}
	</code>
</pre>