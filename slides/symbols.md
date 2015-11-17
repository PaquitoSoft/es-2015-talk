##  Symbols

* Produce unique values
* Is a new primitive type
* Allow for _hidden like_ class properties

<pre>
	<code data-trim>
var MyClass = (function() {

  // module scoped symbol
  var key = Symbol("key");

  function MyClass(privateData) {
    this[key] = privateData;
  }

  MyClass.prototype = {
    doStuff: function() {
      return this[key];
    }
  };

  return MyClass;
})();

var c = new MyClass("hello")
console.log(c["key"]); // undefined
console.log(c.doStuff()); // "hello"

console.log(c[Object.getOwnPropertySymbols(c)[0]]); // "hello"
	</code>
</pre>