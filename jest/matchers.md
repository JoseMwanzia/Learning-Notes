# JEST MATCHERS

## DESCRIPTION
Jest is an open source JavaScript test-runner developed by Facebook. Matchers allow you to test values in diffrent ways.

## USEFULNESS
Allows us to test and evaluate our application

## USE CASES
- Prevents deployment of bad code in production
- Directs developers into achieving minimum requirements for the app.

## EXAMPLE

```javascript

function sum(a, b){
    return a + b;
}

describe('Tests suites', () => {

    const flavor = ["beer", "juice"]

    // toBe() matcher - fro testing equality for primitives.
    test('adds 1 + 2 equal to 3', () => {
        expect(sum(1, 2)).toBe(3)
    })

    // toEqual() matcher - for testing equality for objects and arays
    test('object assignment', () => {
        expect(myData).toEqual({ 'one': 1, 'two': 2 })
    })

    // to make sure an mock function was called
    test('callback function to have been called', () => {
        const callback = jest.fn()
        const flavor = ["beer", "juice"]

        drinkAll(callback, flavor)
        expect(callback).toHaveBeenCalled()
    })

    // make sure a mock function was returned withput throwing an error
    test('drinks returned', () => {
        const drink = jest.fn(() => true)

        drinkAll(drink, flavor)
        expect(drink).toHaveReturned()
    })

    // to test notNull() value
    test('anotherDrink to return with value', () => {
        const beverage1 = { name: 'La Croix (Lemon)' }
        const beverage2 = { name: 'La Croix (Orange)' }

        const drink = jest.fn((beverage) => beverage.name)
        drink(beverage1)
        drink(beverage2)

        expect(anotherDrink()).not.toBeNull()
    })


})

```
## CONCLUSION
The main lesson from this is that matchers are important when it comes to testing for values available in a function.
