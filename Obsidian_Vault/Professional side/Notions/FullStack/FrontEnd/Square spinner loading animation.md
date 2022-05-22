#Frontend

### **Content of the `HTML`page**

```html
<div class=""swapping-squares-spinner :style="spinnerStyle">
	<div class="square"></div>
	<div class="square"></div>
	<div class="square"></div>
	<div class="square"></div>
</div>
```

### **Content of the `CSS`page**

```css
.swapping-squares-spinner, .swapping-squares-spinner * {
	box-sizing: border-box;
}

.swapping-squares-spinner {
	height: 65px;
	width: 65px;
	position: relative;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
}

.swapping-squares-spinner .square {
	height: calc(65px * 0.25 / 1.3);
	width: calc(65px * 0.25 / 1.3);
	animation-duration: 1000ms;
	border: calc(65px * 0.04 / 1.3) solid #FF1D5E;
	margin-right: auto;
	margin-left: auto;
	position: absolute;
	animation-iteration-count: infinite;
}

.swapping-squares-spinner .square:nth-child(1) {
	animation-name: swapping-squares-1;
	animation-delay: 500ms;
}

.swapping-squares-spinner .square:nth-child(2) {
	animation-name: swapping-squares-2;
	animation-delay: 0ms;
}

.swapping-squares-spinner .square:nth-child(3) {
	animation-name: swapping-squares-3;
	animation-delay: 500ms;
}

.swapping-squares-spinner .square:nth-child(4) {
	animation-name: swapping-squares-4;
	animation-delay: 0ms;
}

@keyframes swapping-squares-1 {
	50% {
		transform: translate(150%, 150%) scale(2,2);
	}
}

@keyframes swapping-squares-2 {
	50% {
		transform: translate(-150%,150%) scale(2,2);
	}
}

@keyframes swapping-squares-3 {
	50% {
		transform: translate(-150%,-150%) scale(2,2);
	}
}

@keyframes swapping-squares-4 {
	50% {
		transform: translate(150%,-150%) scale(2,2);
	}
}
```