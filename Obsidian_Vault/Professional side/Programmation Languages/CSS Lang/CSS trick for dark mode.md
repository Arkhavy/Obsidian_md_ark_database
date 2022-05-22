#CSS 

The ability to let your website adjust to the user's theme of choice is a great accessibility feature.

```CSS
/* Light mode */
@media (prefer-color-scheme: light) {
	root {
		--body-bg: #FFFFFF;
		--body-color: #000000;
	}
}

/* Dark mode */
@media (prefer-color-scheme: dark) {
	root {
		--body-bg: #000000;
		--body-color: #FFFFFF;
	}
}
```

In the CSS, --body-bg and --body-olor are CSS variables. As you can see, they contain different values for both modes. In the light theme, I'm setting a white background with black text. In the dark theme, I'm setting black background with white text.

Now if the user's system is set to dark more then the website will appear in dark mode else in light mode