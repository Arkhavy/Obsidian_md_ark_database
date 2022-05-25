#Frontend

### **Content of the `HTML` page**

```html
<div class="content">
	<div class="sun">
		<div class="shadow"></div>
	</div>
</div>
```

### **Content of the `CSS` page**

```css
body {
	background-color: #FFFFFF;
	animation: dayToNight 10s infinite 1.5s;
}

.content {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	display: block;
}

.sun {
	height: 150px;
	width: 159px;
	border-radius: 50%;
	background-color: #FCD25B;
	border: 3px solid #FCD25B;
}

.shadow {
	height: 170px;
	width: 170px;
	border-radius: 50%;
	background-color: #FFFFFF;
	top: -5px;
	left: 0px;
	animation: moveshadow 10s infinite 1.5s;
}

@keyframes moveshadow {
	0% {
		transform: translateX(-170px);
		background-color: #FFFFFF;
	}
	50% {
		transform: translateX(-10px);
		background-color: #000000;
	}
	100% {
		transform: translateX(-170px);
		background-color: #FFFFFF;
	}
}

@keyframes dayToNight {
	0% {
		background-color: #FFFFFF;
	}
	50% {
		background-color: #000000;
	}
	100% {
		background-color: #FFFFFF;
	}
}
```