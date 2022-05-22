#Frontend

### **Content of the `HTML`page**

```html
<!DOCTYPE html>
<html>
	<head>
		<title>
		</title>
	</head>
	<body>
		<div class="hamburger">
			<span class="top-bun"></span>
			<span class="stuffing"></span>
			<span class="bot-bun"></span>
		</div>
	</body>
</html>
```

### **Content of the `CSS`page**

```css
body {
	display: grid;
	place-items: center;
	height:1342px;
	background: #1F2023;
}

.hamburger {
	width: 40px;
	cursor: pointer;
}

.hamburger span {
	width: 100%;
	height: 3px;
	display: block;
	background: #FFFFFF;
	transition: all 0.2s;
	border-radius: 20px;
}

.stuffing {
	margin: 10px 0;
}

.top-bun.active {
	transform: rotate(-45deg) translateX(-9.5px);
	width: 50%;
}

.stuffing.active {
	width: 80%;
	transform: translateX(-3px);
}

.bot-bun.active {
	transform: rotate(45deg) translateX(-9.5px);
	width: 50%;
}
```

### **Content of the `JavaScript`page**

```JavaScript
const	hamburger = document.querySelector(".hamburger");
const	layers = document.querySelectorAll(".hamburger span");

hamburger.addEventListener("click", (e) => {
	layers.forEach((layer) => layer.classList.toggle("active"));
});
```
