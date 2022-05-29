### People slice - usage

```JavaScript
import React, { useEffect } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { getPeople } from '../redux/people';

const People = () => {
	const { data, loading } = useSelector(state=> state.people)
	const dispatch = useDispatch();

	console.log(data)

	useEffect(()=> {
		dispatch(getPeople())
		//eslint-disable-next-line
	}, [])

	if (loading) {
		return <p>loading...</p>
	}

	return (
		<div>
			{data.map(el=> {
				return <p key={el.name}>(el.name)</p>
			})}
		<div>
	);
}

export default People;
```