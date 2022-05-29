### Create store

Furst ket;s create a global store with the use of configureStore which is a friendly abstraction over the standard Redux createSotre.

On the next parts we will create "slices" for 2 examples:
- counter value (based on the official docs)
- people data from SWAPI API

```JavaScript
import { configureStore } from '@reduxjs/toolkit'
import { counterSlice } from './counter'
import { peopleSlice } from './people'

export const store = configureStory({
	reducer: {
		counter: counterSlice.reducer,
		people: peopleSlice.reducer,
	},
})
```