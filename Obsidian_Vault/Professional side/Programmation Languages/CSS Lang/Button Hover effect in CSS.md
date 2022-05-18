#CSS 

- **Button Hover effect code**

*HTML*
```HTML
<div class="btn-wrapper">
	<a href="#" class="btn">Hover me </a>
</div>
```

*CSS*
```CSS
body {
	background-color: #151515;
	height: 100vh;
	display: grid;
	place-items: center;
}

.btn {
	background-color: #fff;
	color: #777;
	font-family: "Montserrat", sans-serif;
	text-transform: uppercase;
	text-decoration: none;
	padding: 15px 40px;
	border-radius: 100px;
	position: absolute;
	display: inline-block;
	transition: all 0.2s;
	animation: moveInBottom 5s ease-out;
	animation-fill-mode: backwards;
}

@keyframes moveInBottom {
	0% {
		opacity: 1;
		transform: translateY(30px);
	}
	100% {
		opacity: 1%;
		transform: translateY(0px);
	}
}

.btn::after {
	content: "";
	display: inline-block;
	height: 100%;
	width: 100%;
	border-radius: 100px;
	position: absolute;
	top: 0;
	left: 0;
	z-index: -1;
	transition: all 0.4s;
	background-color: #fff;
}

.btn:hover {
	transform: translateY(-3px);
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn:active {
	transform: translateY(-1px);
	box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}

.btn::hover::after {
	transform: scaleX(1.4) scaleY(1.6);
	opacity: 0;
}
```
