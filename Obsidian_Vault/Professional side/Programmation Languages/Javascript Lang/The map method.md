#Javascript

Most of the time, we see snippets like this :

```Javascript
const	fruits = ["apple", "orange", "cherry"];
let		text = "";
document.getElementById("main").inerrHTML = text;
fruits.map(i => text += i);
```

IN the above snippet, we are adding fruits text to the DOM in main ID.
It seems there is no issue in the above snippet, though there is one major issue.

Let's understand the issue by definition of map.
map() method creates a new array populated with the results of calling a provided function on every element in the calling array. Using map() method then means returning a new collection of an array.

Example
```Javascript
let	n = [1, 2, 3, 4];
let	add = n.map(i => i + 2);
console.log(add); // [3, 4, 5, 6]
```

As discussed, map() method always returns a new array, so if you don't have any use of a new array then never use map() method.

When you just need to iterate through an array, it is usually recommended using other array methods like forEach or for.of

Example
```Javascript
const	fruits = ["apple", "orange", "cherry"];
let		text = "";
fruits.forEach(myFunction);
document.getElementById("main").innerHTML = text;

function myFunction(item, index) {
	text += index + ": " + item + "<br>";
}
```

#### Why do we care about it ?
As we know, map() method always returns an array. if you just need to update DOM then storing those elements into memory form doesn't add any point.

Of course, for a small chunk of numbers nothing is going to happen, however, if we take a larger number here then it affects the performance side as it will store the value in memory which will be redundant.