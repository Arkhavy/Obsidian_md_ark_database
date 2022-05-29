#Frontend

- **Viewport Tag**

The first and foremost thing to make Responsive Web Design (RWD) is the `<meta> viewport element` or simply called as meta tag. It forces the page to follow the scrren width of the device

```HTML
<meta name="viewport" content="widht=device-width, initial-scale=1.0">
```

- **Dynamic Dimension**

Let's say an element has a width of 500px but the user is viewing on a device having a width smaller than 500px.
In such cases, we use min-width or max-width.

```CSS
min-width: value;
min-height: value;
```

- **Picture Tag**

The HTML `<picture> element` allows you to define different images for different browser window sizes.

```HTML
<picture>
	<source media="(min-width:650px)" srcset="/path">
	<source media="(min-width:465px)" srcset="/path">
	<img src ="/path">
</picture>
```

- **Reponsive text**

Although you can make text responsive using media queries you can also use `viewport`width as well.

```CSS
selector {
	font-size: 10px;
}
```

- **Box sizing**

Small things can make a big impact. `Box-sizing: border-box` forces an element to adjust its padding and border inside width and height of that element.