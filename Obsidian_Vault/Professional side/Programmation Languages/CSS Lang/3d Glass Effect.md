#CSS

### **3D Glass Effect**

```css
.anaglyph {
	letter-spacing: 6px;
	text-shadow: #FF0000 0 0, #00FFFF 0 0;
	transition: text-shadow 200ms;
}

.anaglyph:hover {
	text-shadow: #FF0000 -6px 0, #00FFFF 6px 0;
}
```