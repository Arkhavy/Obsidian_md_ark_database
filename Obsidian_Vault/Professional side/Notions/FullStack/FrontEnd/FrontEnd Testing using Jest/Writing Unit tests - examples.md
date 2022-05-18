3. **Writing Unit tests - examples**

Let's say we need to test that a function used for the concatenation of an array of strings works correctly.

```Javascript
function concat(stringArray)
{
    if (Array.isArray(stringArray)) {
        return stringArray.join('');
    } else throw new Error('Not a valid array!');
}

describe("Concatenate strings method", () => {
    it("should concatenate the array of strings", () => {
        expect(concat(['hello', 'testing'])).toBe('hellotesting');
    })

    it("should throw an error for invalid arrays", () => {
        expect(() => concat('meow')).toThrow('Not a valid array!');
    })
})
```

As you can see, our tests make sure that the code we wrote functions as intended ! We made sure to cover two important cases, and can safely say the function is implemented in a proper way !