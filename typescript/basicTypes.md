# BASIC, LITERAL, AND CUSTOM TYPES

## DESCRIPTION

TypeScript was created to address the challenges of building large-scale JavaScript applications and adds optional type annotations, classes, interfaces, and other features to the language. Benefits include; Type Safety, Improved Tooling, Improved Maintainability, Backwards Compatibility.

## USEFULNESS

TypeScripts key benefit compared to JavaScript is its scalability. When dealing with applications, managing JavaScript can get complicated, leading to errors. 

## EXAMPLE

``` typescript
    let myName: string = 'Bob' // Basic type
    const myName2 = 'Bob' // Literal Type - string

    type Address = {
        street: string
        city: string
        country: string
    }
    type Person = { // Custom types
        name: string
        age: number
        isStudent: boolean
        address?: Address // nested Object Types, Optional Properties
    } 

    let person1: Person = {
        name: "Joe",
        age: 42,
        isStudent: true,
    }    
```

## CONCLUSION

Basic types form the core building blocks of more complex types.
