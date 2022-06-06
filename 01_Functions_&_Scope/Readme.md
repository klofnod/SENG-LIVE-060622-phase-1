# Functions
## SWBAT
- [ ] Describe what functions are and their central importance in JS
- [ ] Review syntax differences between regular functions and arrow functions
- [ ]Explain the difference between:
    - [ ] Block scope
    - [ ] Function scope
    - [ ]Global scope
- [ ] Understand what it means that a function are first- class -objects
- [ ] Explain what a higher-order function is
- [ ] Grasp the relationship betweenDescribe what a callback and higher-order functions is

<p align="center">
    <img src="../assets/functions.jpeg" width="250" height="250">
</p>

## Deliverables 

The owner of a small bookstore has hired your to build them an app to help keep track of their book inventory. 

1. Store the bookstore name, books and their prices into variables.

2. Write a function to open/close the store and greet customers.

3. Write a function that displays books and their current promos.

4. Write a function that buys a book, clears it from its variable and returns a customer their total. 

## Functions
Functions are like a little program. They consist of a set of statements/tasks and return a value or undefined. 

```
// This is a function delcoration 
// This function is returning the string of 'hi'
function sayHi() {
    return 'hi'
}
//This is a function reference but it doesn't actually run the function. 
sayhi

// To run or call or invoke (all the same thing). Write the functions name and add a pair of ()
sayHi()

// This functions console.logs the string of 'hello' but returns undefined because it does not have the return keyword.

function sayHello(){
    console.log('hello')
}

sayHello()

// logging and returning are not the same thing. A return value becomes the value of an invoked function, while a console.log only logs something to the console. 

```

Functions can take unique localized variables called parameters. When the function is invoked, it's passed an argument that becomes the parameter's value.

```

function squareNumb(num){
    //num is the parameter, it is scoped to the inside of the function
    return num*num
}
// 2 is the argument. The value of num in the above function becomes 2.
squareNumb(2)


// functions can take multiple parameters.
function addTwo(num1, numb2){
    return num1 + num2
}
addTwo(5,10)

```

Arrow functions are another way to declare functions with some added benefits.

```
// An arrow function can avoid {} if it's return done on a single line or with () 
// An arrow function with a single paramater doesn't need the () around the paramater. 
const faveFood = food =>  `My fave food is ${food}`
const faveFood = food => (
     `My fave food is ${food}`
)
faveFood('cookies')

```

Arrow functions also have the added benefit of passing context, but we won't be covering that today. 

## Callbacks and HigherOrder Functions 

Functions in JavaScript are treated like any other variable. When functions are treated like this, we refer to them as First class. One of the most significant benefits of this is that functions in JavaScript can be passed as arguments to other functions.

```
// A function that returns a function is called a Higher-Order Function.

const outsideFunction = () => {
    return () => {
        //inside function
    }
}

//A function that is taken as an argument is a callback 

const opening => (openingVideo, credits){
    return openingVideo(credits)
}

const taskingHistory(){
    //... video functionality here
}

const crashCourse(){
    //... video functionality here
}

opening(crashCourse, 'Hank Green')

```
