- Using `:is` to chain selectors
>When you want to apply the same styling to more than one state of an element, you can select all of these states without repeating the base selector by using `:is` !

Before
```css
button:focus,
button:hover,
button[aria-current="page"] {
	outline: 3px solid lightgreen;
}
```

After
```css
button:is(:focus, :hover, [aria-current="page"]) {
	outline: 3px solid lightgreen;
}
```

This allows you to write less CSS by avoiding code repetition.