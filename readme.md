# Day-1 INTERVIEW QUESTIONS

## Difference between “ == “ and “ === “ operators.
In JavaScript, the "==" operator is used to compare the values of two operands, whereas the "===" operator is used to compare both the values and the data types of the operands.

Here's an example to illustrate the difference:

let a = 5;

let b = "5";

console.log(a == b); // true

console.log(a === b); // false
<hr>

## What are the differences between var, let and const?
In JavaScript, 'var', 'let', and 'const' are keywords used to declare variables. While they might seem similar, they have some important differences:
1. 'var' declarations are globally scoped or function scoped while 'let' and 'const' are block scoped.
2. 'var' variables can be redeclared and updated while 'let' and 'const' variables cannot be redeclared (in the same scope) and 'const' variables cannot be updated.

Here's an example code that demonstrates these differences:

// var example

var x = 10;

if (true) {

  var x = 20;

}

console.log(x); // outputs 20


// let example

let y = 10;

if (true) {

  let y = 20;

}

console.log(y); // outputs 10


// const example

const z = 10;

// z = 20; // throws an error

console.log(z); // outputs 10
<hr>

## What is hoisting?
Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their respective scopes during the compilation phase, before the code is actually executed. This means that even if a variable or function is declared after it is used, it can still be accessed.

For example:

x = 5;

console.log(x);

var x;
<hr>

## What is a Temporal Dead Zone?
In JavaScript, a Temporal Dead Zone (TDZ) is a period of time during the code execution where a variable exists in the scope but cannot be accessed due to a restriction known as "temporal dead zone". The TDZ occurs for let and const variables, which are block-scoped variables that cannot be accessed before they are declared.

Here's an example code:

console.log(x); // throws ReferenceError: x is not defined

let x = 10;
<hr>

## What is meant by first class functions
In JavaScript, first class function means that functions can be assigned to variables, passed as arguments to other functions, and returned from functions like any other data type.

Now, let's see how first-class functions can be used in JavaScript :

function multiplyByTwo(num) {

  return num * 2;

}


function callWith10(func) {

  return func(10);

}


let result = callWith10(multiplyByTwo); // returns 20
<hr>

## What are pure functions?
Pure functions are functions that always return the same output for a given input and do not have any side effects, meaning they do not modify any variables or states outside of the function.

Here's an example of a pure function in JavaScript:

function add(a, b) {

  return a + b;

}


