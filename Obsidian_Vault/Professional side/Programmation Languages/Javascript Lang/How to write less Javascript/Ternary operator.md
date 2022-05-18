- **Ternary operator**
*Before*
```Javascript
let isAdult;
if (age > 17) {
	isAdult = true;
} else {
	isAdult = false;
}
```
*After*
```Javascript
let isAdult = age > 17 ? true : false;
```