#CSS

### **Non rectangular section**

```css
.header {
	padding-bottom: 15px;
	clip-path:
	polygon(
		0%, 0%,
		100%, 0%,
		100% calc(100% - 15px),
		0% 100%
	);
}
```