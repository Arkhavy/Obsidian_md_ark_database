#Frontend

### **Content of the `HTML` page**

```html
<section class="cards">
	<figure class="card">
		<figcaption class="card-title">Ouaf</figcaption>
	</figure>
</section>
```

### **Content of the `CSS` page**

```css
.cards {
	perspective: 500px;
}

.card {
	width: 200px;
	height: 250px;
	background: url('./image.png') center no-repeat;
	background-size: cover;
	border: 1px solid #FFFFFF40;
	border-radius: 4px;
	position: relative;
	transform-style: preserve-3d;
	will-change: transform;
	transition: transform .5s;
}

.card:hover {
	transform: translateZ(10px) rotateX(20deg) rotateY(30deg);
}

.card-title {
	color: #FFFFFF;
	position: absolute;
	top: 50%;
	right: 10px;
	transform: translateY(-50%);
	transition: transform .5s;
}

.card:hover .card-title {
	transform: translateZ(50px);
}
```