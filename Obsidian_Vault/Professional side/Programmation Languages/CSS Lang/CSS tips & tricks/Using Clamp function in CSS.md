- Clamp - Wirte fewer media queries
>By using the clamp() function, you can configure an element to occupy a minimum, preferred & maximum amount of space inside its parent container !

```css
.element {
	width: clamp(250px, 50%, 500px);
}
```

In this example, we would prefer the width to be 50% of the parent element, but since that would go over the limit of 500px, it stops growing at that limit. If we resized the parent to a smaller size, the element would also get smaller up until the point it reaches its min width, unable to become any smaller.