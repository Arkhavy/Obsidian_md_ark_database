2. **Mark Up The HTML**
In the HTML, add the dark mode switch at the top of the page. Then, create a `<h1>` tag for the title and a semantic `<article>` tag for the content of the page. Finally, add the two `<script>` tags right before the closing `</body>` tag.

Pay attention that you add the `jQuery library` before the custom script so that it can use its functionalities. The `style.css` file goes into the `<head` section of the page.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>DEMO | Dark Mode in CSS</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="switch">Dark mode:
            <span class="inner-switch">OFF</span>
        </div>
        <h1 class="title">Animals</h1>
        <article>
            <h1>Ouaf</h1>
            <p>watermelon</p>
            <img src="ouaf.png">
        </article>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
        <script src="script.js"></script>
    </body>
</html>
```