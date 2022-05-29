### Create slice - people

To handle async call we need some sort of async middleware. In traditional Redux we would use Redux thunk. With Redux toolkit we can use the createAsyncThunk API to perform asynchronous tasks.

createAsyncThunk will generate three Redux action creators unsing createAction : pending, fulfilled and rejected that will be handled in extraReducers with the use of the "builder callback" notation.

```JavaScript
import { createAsyncThunk, createSlice } from '@reduxjs/toolkit'
import axios from 'axios';

const initialState = {
	data: [],
	status: null,
	loading: false,
}

export const getPeople = createAsyncThunk(
	'people/getPeople',
	async (_, thunkAPI) => {
		const response = await axios.get('https://swapi.dev/api/people/');
		return await response.data;
	}
);

export const peopleSlice = createSlice({
	name: 'people',
	initialState,
	reducers: {},
	extraReducers: (builder) => {
		builder
			.addCase(getPeople.pending, (state, action) => {
				state.status = 'Pending';
				state.loading = true;
			})
			.addCase(getPeople.fulfilled, (state, action) => {
				state.status = 'Fullfilled';
				state.data = action.payload.results;
				state.loading = false;
			})
			.addCase(getPeople.rejected, (state, action) => {
				state.status = 'Rejected';
				state.loading = false;
			})
	}
})
```