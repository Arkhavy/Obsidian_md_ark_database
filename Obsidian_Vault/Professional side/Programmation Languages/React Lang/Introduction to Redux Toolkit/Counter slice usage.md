### Counter slice - usage

Let's take a look how we can use our configuration in a counter component

```JavaScript
import React from 'react'
import { useSelector, useDispatch } from 'react-redux'
import { decrement, increment, incrementByAmount } from '../redux/counter'

const Counter = () => {
	const countValue = useSelector((state) => state.counter.value)
	const dispatch = useDispatch()

	return (
		<div>
			<div>
				<h3>(countValue)</h3>
				<hr />
				<button
					aria-label="Increment value"
					onClick={() => dispatch(increment())}
				>
					Increment
				</button>
				<button
					aria-label="Decrement value"
					onClick={() => dispatch(decrement())}
				>
					Decrement
				</button>
				<button
					aria-label="Decrement value"
					onClick={() => dispatch(incrementByAmount(10))}
				>
					Increment by 10
				</button>
			</div>
		</div>
	)
}

export default Counter
```