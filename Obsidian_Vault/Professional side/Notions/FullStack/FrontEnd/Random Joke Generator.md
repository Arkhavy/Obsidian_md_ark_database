#Frontend

### **Content of the `HTML`page**

- Content of the `<head>`
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
```

- Content of the `<body>`
```html
<div class="container">
	<h1>Random Joke Generator</h1>
	<p id="joke">
		Ouaf.
	</p>
	<button type="submit" class="btn" onclick="fetchJoke()">
		New Joke
	</button>
</div>
```

### **Content of the `CSS` page**
```css
* {
	font-family: 'Poppins', sans-serif;
}

body {
	background-color: #111827;
	color: #FFFFFF;
	display: flex;
	align-items: center;
	justify-content: center;
}

.container {
	display: flex;
	flex-direction: column;
	align-items: center;
	border: 2px solid #00BFFF;
	padding: 40px;
	border-radius: 20px;
	width: 480px;
}

#joke {
	font-style: italic;
}

.btn {
	height: 48px;
	width: 128px;
	border: 2px solid #00BFFF;
	background: #00BFFF;
	color: #FFFFFF;
	font-size: 16px;
	border-radius: 7px;
	padding: 8px;
	margin-top: 30px;
	cursor: pointer;
}
```

### **Content of the `JavaScript` page**
```Javascript
const fetchJoke = async () => {
	let response = await fetch("https://api.chucknorris.io/jokes/random");
	let data = await response.json();
	document.getElementByID("joke").innerText = data.value;
}
```