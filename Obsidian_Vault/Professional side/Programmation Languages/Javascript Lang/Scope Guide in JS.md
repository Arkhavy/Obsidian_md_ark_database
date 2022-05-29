#Javascript

Scope defines the accessibility of the variable, which means whether the variable is accessible or not.
There is three types of scopes :

### **Block scope**

Variable which is defined by let and const in a block `{}` are only accessible to that block.

```Javascript
{
	let content = 'ouaf';
	console.log(content); // accessible here
}
console.log(content); // not accessible here, will give ReferenceError
```

### **Function scope**

Any variable which is defined inside the function is only accessible inside that function, doesn't matter you defined with let, const or var.

```Javascript
(function CreateOuaf() {
	var ouaf = "ouaf";
	console.log(ouaf); // accessible here
})
console.log(ouaf); // not accessible here
```

### **Global scope**

Any variables defined outside a function or block are globally accessible, which means the variables are in the global scope.

```Javascript
var ouaf = "Hello ouaf";
(function createOuaf() {
	console.log(ouaf); // accessible here
})();
{
	console.log(ouaf); // accessible here
}
console.log(ouaf); // accessible here
```