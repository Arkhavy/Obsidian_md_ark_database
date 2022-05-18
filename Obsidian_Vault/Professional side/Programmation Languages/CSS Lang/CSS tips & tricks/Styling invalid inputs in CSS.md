- Quickly styling invalid inputs
>You can quickly apply different styling depending on your input's validation state when using the required attribute. We can check for multiple conditions such as `:placeholder-shown` by using the `:where` selector and negate the condition by using the `:not` selector.

```css
:required:where(input):where(:not(:placeholder-shown, :invalid)) {
	outline: 2px solid green;
}

:required:where(input):where(:placeholder-shown, :invalid) {
	outline: 2px solid red;
}
```

The input's styling will update depending on whether it is valid or not in our application.

This is not the beest way to validate inputs, but it's a cool trick to know if you ever need it.