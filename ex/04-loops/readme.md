# Looping

In programming, any time we need a statement to repeat, we use a construct called a __loop__. Loops are used to [iterate](https://www.merriam-webster.com/dictionary/iteration), or perform an action repeatedly. 

If we have an array `let myArray = [1, 2, 3, 4, 5]`

and we want to pring out ever value, we _could_ do so by repeatedly logging each index as such
```
    console.log(myArray[0])
    console.log(myArray[1])
    console.log(myArray[2])
    console.log(myArray[3])
    console.log(myArray[4])
```
but say this array had 100 or 1,000 or 10,000 values, it would be very inefficient to do this for each value. instead, we would use a loop following the syntax

    for(let i = 0; i < myArray.length; i++){
        console.log(myArray[i])
    }


a for loop consists of three statements separated by semicolons

- declaration of iterator
- definition of condition
- what to count by

inside of the parenthesis following the keyword `for` we have
```
    let i = 0
    i < myArray.length
    i++
```
the first statement `let i = 0` is declaring our iterator, or counter
you can declare this to be any number, it is the number at which we start counting
```
    i < myArray.length
```
is the condition that is checked after each time the loop completes
the computer will evaluate this statement, and if true, execute the logic defined in the loop
if the statement is false, the loop will stop executing
```
    i++
```
is the number by which we increase our counter after each round of the loop completes. `i++` is shorthand for `i += 1` which is shorthand for `i = i + 1`
what this means is, after the loop completes, increase our counter by one.
in psuedocode, the above for loop is accomplishing:
```
    for(start counting at 1; while it is true that our counter is less than the length of myArray; increasing counter by one after each round){
        //execute the logic defined here
        console.log(myArray[indexed at the current value of counter])
    }
```