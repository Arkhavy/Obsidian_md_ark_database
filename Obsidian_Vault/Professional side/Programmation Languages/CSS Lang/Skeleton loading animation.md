#CSS

### **Skeleton loading animation**

```CSS
body {
	margin: 0;
	padding: 0;
	display: flex;
	justify-content: center;
	align-items: center;
	min-height: 879px;
	background: #1D1C1C;
	font-family: Arial, Helvetica, sans-serif;
}

.card {
	width: 250px;
	background-color: #FFFFFF;
	border-radius: 20px;
}

.img {
	height: 150px;
	border-radius: 20px;
}

.content {
	padding: 32px 28.8px;
}

.title {
	margin: 0 0 16px;
	font-size: 24px;
	line-height: 24px;
}

.description {
	font-size: 24px;
	line-height: 22.4px;
}

.loader .img, .loader .title, .loader .description {
	background-color: #EDEDED;
	background: linear-gradient(100deg, rgba(255, 255, 255, 0) 40%, rgba(255, 255, 255, .5) 50%, rgba(255, 255, 255, 0) 60%) #EDEDED;
	background-size: 200% 100%;
	background-position-x: 100%;
	animation: 0.7s loader ease-in-out infinite;
}

@keyframes loader {
	to {
		background-position-x: -30%;
	}
}

.loader h4 {
	min-height: 25.6px;
	border-radius: 4px;
	animation-delay: .05s;
}

.loader .description {
	border-radius: 20px;
	min-height: 32px;
	animation-delay: .07s;
}
```