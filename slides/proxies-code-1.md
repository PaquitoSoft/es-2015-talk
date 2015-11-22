##  Proxies code - I

<pre>
	<code data-trim>
let person = window.person = new Observable({
	name: 'Rollo Tomassi',
	age: 47
});

person.onPropertyChanged(function(property, prev, current) {
	console.info(`Changing property: ${property}. From (${prev}) to (${current})`);
});

person.age = 48;
person.age++;
	</code>
</pre>