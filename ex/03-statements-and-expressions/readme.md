# Statements & Expressions

Data types and operators are the basic building blocks of programming. A computer though, can only only understand one task at a time. To accomplish more complex tasks, we string together variables and operations to form _statements_ and _expressions_. 

In the same way that mathematical expressions _evaluate_ based on an order of operations, logical statements do so in the same way.

## Chaining Statement & Expressions

In order to accomplish complex tasks we must begin to chain these logical statements together. When a complex statement is present in logic, the computer will walk through step by step, performing one operation at a time, until there are no more operations to be performed. 

the expression 
```
    let myValue = 10
    let myOtherValue = 5 

    let myVariable = myValue * (myOtherValue * myValue)
```
would assign the value `500` into `myVariable`, evaluating what is inside of the parenthesis first so that the expression becomes `let myVariable = myValue * 50` then  `let myVariable = 10 * 50`

any number of statements and expressions can be chained together to accomplish whatever operations and calculations you like.

## If Statements
the most common statement you will use is the _if_ statement. An if statement will _evaluate_ the expression (or walk through it, step by step, resolving each step following order of operations) in the following parenthesis and act accordingly. You can think of if statements as following the logic `if (this is true) then { perform this action } else { do something else}`

if statements can be chained together, following the syntax 
```    
    If(condition){
        //logic
    }else if(another condition){
        //other logic
    }else{
        //logic to fire if none of the defined conditions are met
    }


    if(1 < 2){ 
        console.log(true) 
    }
```
will print __true__ to the console. You can use variables inside of the if statement to allow the program to determine what branch of the logic should run dynamically.
```
    let shouldRun = false

    if(shouldRun)
    {
        console.log('Is your refrigerator running?')
    }else{
        shouldRun = true
    }
```
will not pring _anything_ to the console. On run, the program will check take the value stored in variable `shouldRun` and insert it in the place of the variable, so the code then becomes
```
    if(false)
    {
        console.log('Is your refrigerator running?')
    }else{
        shouldRun = true
    }
```
what would happen the second time this if statement checks shouldRun?
