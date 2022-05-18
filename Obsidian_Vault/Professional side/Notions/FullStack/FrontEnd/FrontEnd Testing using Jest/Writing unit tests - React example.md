4. **Writing unit tests - React example**

Let's take it a step further, now we will write some unit tests for a React counter component that we created.

```Javascript
import Enzyme, { shallow } from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';
import Counter from './Counter';
import App from './App';

Enzyme.configure({ adapter: new Adapter() });

describe('Counter component', () => {
    it('renders the component successfully', () => {
        const app = shallow(<App />);
        expect(app.find(Counter)).toBeTruthy();
    });

    it('should increment the counter', () => {
        const wrapper = shallow(<Counter />);
        const incrementBtn = wrapper.find('button');
        const count = wrapper.find('p').text();

        expect(count).toEqual('0');

        incrementBtn.simulate('click');
        expect(count).toEqual('1');
    });
})
```

```Javascript
const Counter = () => {
    const [counter, setCounter] = useState(0);
    const incrementCounter = () => {
        setCounter((count) => count + 1);
    };
  
    return (
        <>
            <button onCLick={incrementCounter}>
                +
            </button>
            <p>{counter}</p>
        </>
    );
}
```

We use Enzyme to simulate rendering & certain events in our component. With this technique we can test multiple behaviours and cover all the relevant cases.