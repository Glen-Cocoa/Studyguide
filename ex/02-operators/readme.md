# Operators
Operators are just characters used to give the computer instructions. 
In JavaScript we have operators for
- addition
- subtraction
- multiplication
- division
- increment
- decrement
- negation
- assignment

## Addition
Used to add values together. With numbers will add the values. Used on strings the values will be concatenated.
 ```   
    1 + 1 === 2 //true

    'str' + 'ing' === 'string' //true
```
## Subtraction
Used to subtract numeric values.
```
    10 - 5 === 5 //true
````
## Multiplication
Used to multiply numeric values
```
    10 * 10 === 100 //true
```
## Division
Used to divide numeric values
```
    10 / 2 === 5 //true
```
## Increment
Shorthand for increasing a numeric value by one.
```
    5++ === 6 //true
```
technically the same as 
```
    5 += 1
```
which is shorthand for 
```
    5 = 5 + 1
```
## Decrement
Shorthand for decreasing a numeric value by one.
```
    5-- === 4 //true
```
technically the same as 
```
    5 -= 1
```
which is shorthand for 
```
    5 = 5 - 1
```
## Negation
Used to negate, or flip the value of whatever it is applied to.
```
    !true === false //true
    !false === true //true
```
## Assignment
Used to _assign_ a value.
```
    const myValue = 10
    
    myValue === 10 //true
```
## Comparison/Equality Check
Used to see if two values are the same. Double equals checks if value is a match. Triple equals checks for a match of value _and_ type. For this reason triple equals is _almost always_ prefereable.
```
    let numValue = 1
    let stringValue = '1'

    numValue == stringValue //true
    numValue === stringValue //false
```
