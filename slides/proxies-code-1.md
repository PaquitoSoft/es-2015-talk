##  Proxies code - I

<pre style="width: 100%;">
	<code data-trim>
let person = new Observable({
	name: 'Rollo Tomassi',
	age: 47
});

person.onPropertyChanged(function(property, prev, current) {
	console.info(`Changing property: ${property}...`);
	console.info(`From (${prev}) to (${current})`);
});

person.age = 48;
person.age++;
	</code>
</pre>