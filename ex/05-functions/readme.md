# Functions
Functions are the meat and potatos of JavaScript development. They are a way of defining a set of operations to be performed that can then be called or _invoked_ again without having to repeat the same logic. Functions are noted by the syntax:
```
    function myFunction (){
        //function logic
        //operations go here
        console.log('running!')
    }
```
This function would be be callable, or _invokeable_ using the syntax `myFunction()` which would print to the console `running!`

## Arguments/Parameters

When using functions, sometime we want to be able to have our program determine a target value inside of a function dynamically. To do so, we define our function with arguments/parameters following the syntax
```
    function functionWithParams (param){
        console.log(param)
    }
```
We would refer to the variable above `param` as the functions parameter. This name is defined by you, the programmer, while you are defining the function, and can be just about anything. Upon being invoked, the each instance of the parameter is replaced with the value passed in.
```
    functionWithParams('foobar')
```
would print `'foobar'` to the console.

```
    function logLarry(larry){
        console.log(larry)
    }
```
is perfectly valid syntax, and calling `logLarry('any string value')`

would print `any string value` to the console

functions can be defined with multiple parameters, of any data type.

## Scope

Scope is a complex topic, but to start you can think of it as what logic can access what values. In JavaScript there is _local_ scope and _global_ scope. A value that has _global_ scope is accessible from anywhere (and generally bad practice. If you'd like to know why, read [this](https://dev.to/mervinsv/why-global-variables-are-bad-4pj) article). A value that has local scope is only accessible from within the function in which it is declared.
```
    let globalVariable = 10

    console.log(globalVariable)
```
will print `10` to the console.
```
    function functionScope(){
        let localVariable = 10
    }  

    console.log(localVariable)
```
will print `undefined` to the console, because `localVariable` is _outside the scope_ of where it is being called.

functions that are being called within other functions though, have access to the values defined in the same function scope that they are.
```
    function funcOne(){
        let localVar = 'value'
        funcTwo()
    }

    function funcTwo(){
        console.log(localVar)
    }
```
calling `funcOne()` would print out `'value'` to the console. It is better practice though to pass the value as a parameter where possible, such as is done in the below example:
```
    function funcOne(){
        let localVar = 'value'
        funcTwo(locaVar)
    }

    function funcTwo(someArg){
        console.log(someArg)
    }
```
Functions can be chained together in the above example to make sure actions are taken is a specific order, and doing so generally makes for more organized, easier to read code.

## Callback Functions
This section is taken directly from the dusty-learning JS supplement repo [here](https://github.com/dusty-learning/supplement/tree/master/JavaScript/Functions), which is an extremely detailed and helpful resource. I would highly recommend going over everything he has included.

So another use for functions is what's known as a callback function. These are functions that are triggered once the called function finishes. (Sounds confusing I know)

Callback functions can usually be passed along to a function as a parameter
```
    var something = function(cb, list) {
    cb(3 * list.length);
    };
```
In the above example I used the param cb (acronym for callback in this case) and a param of list, so we create a new result by taking the list length and multiplying it by 3.

Now yes this doesn't need a callback this is strictly for example sake.

A good example of callbacks are the use of functional iterators which are functional ways of looping.
```
    var dataList = [1, 2, 3, 4, 5];

    // This will create a new array from dataList but every value will be doubled
    var doubled = dataList.map(function(val) {
     return val * 2
    });

    console.log(doubled); // => [2, 4, 6, 8, 10]

    // This will take an "accumulator" (acc) and add the value of each number in our data list to it
    // Notice the 0 after the function this sets the initial value of acc
    var sum = dataList.reduce(function(acc, val) {
    return acc + val;
    }, 0);

    console.log(sum); // => 15
```
These are examples of 2 different functional iterators I use these as much as I possibly can instead of your classic for loop.

There's a lot of these out there I suggest checking out MDN on each one for more info (I will make a supplamental piece on them too) some of the others are: forEach, filter, and find each one does something a little different to make life easier.

A callback is essentially just a way of moving data along once a function is finished they're more useful in async environments which we will get more into later.