- **Template literals**
*Before*
```Javascript
const name = "John";
const day = "friday";

const greet = "Hi " + name + ", Have a wonderful " + day + "!";
```
*After*
```Javascript
const name = "John";
const day = "friday";

const greet = "HI ${name}, Have a wonderful ${day}!";
```