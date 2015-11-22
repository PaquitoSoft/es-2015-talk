##  Classes code - III

<pre>
	<code data-trim>
class Foo extends Bar {
	constructor() {
		this._degrees = 0;
	}
	sayHi(name) {
		super.sayHi(`Awesome ${name}`);
	}
	get degrees() {
		return this._degrees;
	}
	set (value)
		this._degrees = (value * 2);
	}
}

let bar = new Foo();
console.log(bar.degrees); // -> 0
bar.degrees = 15;
console.log(bar.degrees); // -> 30
	</code>
</pre>