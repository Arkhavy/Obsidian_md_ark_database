#Javascript

- **Javascript Objects**

Javascript object is a non-primitive data-type that allows you to store multiple collections of data.
```JavaScript
const student = {
	firstName: 'Loïc',
	promotion: 2021
};
```

Here, `student` is an object that stores values such as `strings` and `numbers`.

- **Object declaration**

The syntax to declare an object is
```Javascript
const	object_name = {
	key1: value1,
	key2: value2
};
```
Each member of an object is a `key:value` pair separated by commas and enclosed in curly braces {}.

- **Object properties**

In JavaScript, `key:value` pairs are called properties. `key1: value1` is a property.

- **Accessing properties**

You can acces the `value` of a property by using its key.

- Using dot notation : `objectName.key`
- Using bracket Notation : `objectName["key"]

- **Nested Objects**

An object can also contain another object.
```Javascript
const student = {
	name: 'John',
	age: 20,
	marks: {
		science: 70,
		maths: 75
	}
}
```

we can then access values the same way using as example `student.marks.science` to get the science value.

- **Object methods**

An object can also contain a function.

```JavaScript
const person = {
	name: 'Sam',
	age: 30,
	greet: function() {
		console.log('Hello')
	}
}

person.greet(); // Hello
```

Here, a function is used as a value for the greet key, that's the reason why we need to use `person.greet()` with parenthesis to call the function inside the object.

