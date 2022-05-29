### Create slice - counter

createSlice accepts a single configuration object parameter which contains:
- name -> used in action types
- initialState -> initial state for the reducer
- reducers -> to generate actions by key names
- extreaReducers -> to reference "external" actions

```JavaScript
import { createSlice } from '@reduxjs/toolkit'

const initialState = {
	value: 0,
}

export const counterSlice = createSlice({
	name: 'counter',
	initialState,
	reducers: {
		increment: (state) => {
			state.value += 1
		},
		decrement: (state) => {
			state.value -= 1
		},
		incrementByAmount: (state, action) => {
			state.value += action.payload
		},
	},
})

export const { increment, decrement, incrementByAmount } = counterSlice.actions
```