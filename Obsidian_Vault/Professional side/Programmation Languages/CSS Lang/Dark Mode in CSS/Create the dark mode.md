5. **Add the CSS for the Dark Mode**
The last thing you need to do is defining some styles for the `.dark class` added to the HTML by the jQuery script above when dark mode is switch on. Besides the `.dark class`, laso apply the dark mode theme to all of its direct and indirect children by using the `.dark * universal CSS selector`.

```css
.dark,
.dark * {
	background-color: #222;
	color: #e6e6e6;
	border-color: #e6e6e6;
}
```