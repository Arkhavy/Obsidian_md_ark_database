3. **Create the light mode**
First, let's create the CSS for the light mode, as this is the default state of the page. The CSS on the next page makes use of a column-based `flexbox layout` that enables you to easily position elements on the page, specifically the `switch` class that handles the wrapper of the dark toggle and the `<img>` elements.

The `display: flex` rule added to the `<body>` tag makes it possible to use the `align-self: flex-end` rule on the dark mode switch.

In this way, the switch is automatically positioned to the top right corner of the flex container at all viewport sizes.

Similarly, the `display: flex` and `flex-direction: column` rules added to the `<article>` tag make it possible to use the `align-self: center` rule on all the images inside the article.

```css
body {
    font-family: sans-serif;
    font-size: 1.125rem;
    display: flex;
    flex-direction: column;
    max-width: 50rem;
    margin: 0 auto;
    padding: 0 0.9375rem;
}

small {
    font-style: italic;
}

article {
    display: flex;
    flex-direction: column;
}

img {
    max-width: 100%;
    display: block;
    align-self: center;
}

.switch {
    align-self: flex-end;
    margin: 0.9375rem;
}

.inner-switch {
    display: inline-block;
    cursor: pointer;
    border: 1px solid #555;
    border-radius: 1.25rem;
    width: 3.125rem;
    text-align: center;
    font-size: 1rem;
    padding: 0.1875rem;
    margin-left: 0.3125rem;
}
```