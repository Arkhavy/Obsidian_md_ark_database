- Using the Aspect Ratio property
>You can use the aspect-ratio property to quickly manage the relationship between the width and height of an element or to build responsive containers that will always respect the aspect ratio they are configured to fill.

```css
.square {
	width: 200px;
	aspect-ratio: 1;
}
```

For the `.square` class, since the aspect ratio is 1, the height will always match the width, creating a square.

```css
.video {
	width: 100%;
	apsect-ratio: 16/9;
}
```

For the `.video` class, the video will always be 100% of the parent container, but it will also always respect the 16:9 aspect ratio on resize.