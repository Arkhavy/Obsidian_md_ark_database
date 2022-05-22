#React

### **Introduction of React JSX**

Here, we will learn about React.js JSX with use of example.

#### **What is a JSX ?**

JSX stands for JavaScript XML. It is used in React to easily write HTML and Javascript together.

```javascript
const	element = <h1>This is a header</h1>;
```

This funny tag syntax is neither a string nor HTML. It is called JSX, and it is a React XML.
JSX might seem awkward at first, but you get used to it pretty fast.
React keeps both HTML and Javascript code in same file.
We can use the previous JSX code in React like this:

```javascript
class JSXDemo extends React.Component {
	render(){
		return <h1>This is a header</h1>;
	}
}
```

### **Expressions in JSX**

With JSX, you can write expressions inside curly braces.
The expression can be a React variable, or property, or any other valid JavaScript expression.

```javascript
const	name = "ouaf";
const	myElement = <h1>This is a header</h1>;
```

### **Top level element**

In JSX, the HTML code must be wrapped in one top level element.
If you want to write two paragraphs, you must put them inside a parent element, like a div element.

```javascript
const	myElement = (
	<div>
		<p>Ouaf 1</p>
		<p>Ouaf 2</p>
	</div>
);
```

Alternatively, you can use a `fragment`to wrap multiple lines.
This will prevent unnecessarily adding extra nodes to the DOM.
A fragment looks like an empty HTML tag: `<> </>`

- Elements must be closed:
JSX follows XML rules, and therefore HTML elements must be properly closed.
```javascript
const	myElement = <input type="text" />;
```

`Attribute class = className`is rendered as Javascript, and the class keyword is a reserved word in JS, you are not allowed to use it in JSX.
JSX solved this by using className instead.

```javascript
const	myElement = <h1 className="ouaf">meow</h1>
```