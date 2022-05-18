#React

With classes
React class based components are the bread and butter of most modern web apps built in ReactJS:
```ReactJS
import React from "react";

class App extends React.Component
{
	render()
	{
		return <h1>@arkhavy</h1>;
	}
}

export default App;

```


With Function
Example of a Functional Component in React defined as App which returns JSX:
```ReactJS
import React from "react";

function App()
{
	const greeting = "Hello arkhavy";

	return <h1>{greeting}</h1>;
}

export default App;
```


With arrow function
Arrow-functional components are kind of similar to the functional components with a small difference:
```ReactJS
import React from "react";

const App = () =>
{
	return
	{
		<div>
			Something here.
		</div>
	};
}

export default App;
```