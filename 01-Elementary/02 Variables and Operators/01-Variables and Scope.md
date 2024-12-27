# Questions

- 01 Define Variables?
- 02 What are the different ways of declaring variables?
- 03 Explain variable Declaration.
- 04 How to declare multiple variables in a single line?
- 05 Explain Variable Assignment.
- 06 How to declare and assign a variable at the same time?
- 07 What is a scope?
- 08 What are the different Scopes in JS?
- 09 Explain all the scopes in detail.
- 10 Explain the lifetime of JS Variables.

# Variables

- In JavaScript, a variable is essentially a `container of data`,
- which are used to `store data values`
- that can be `referenced` and `manipulated` throughout a program.
- Variables allow you to `label` data with a descriptive name,
- so it can be used and `updated` easily.

## Variable Declaration

To create a variable, you use a variable declaration. This tells JavaScript to allocate memory to store the value.

JavaScript Variables can be declared in 4 ways:

- Automatically
- Using var
- Using let
- Using const

### Automatically

In this first example, x, y, and z are undeclared variables.

They are automatically declared when first used:

```JS
x = 5;
y = 6;
z = x + y;
```

It is considered good programming practice to always declare variables before use.

From the examples you can guess:

- x stores the value 5
- y stores the value 6
- z stores the value 11

### Using var

```JS
var x = 5;
var y = 6;
var z = x + y;
```

The var keyword was used in all JavaScript code from 1995 to 2015.

The let and const keywords were added to JavaScript in 2015.

The var keyword should only be used in code written for older browsers.

### Using let

```JS
let x = 5;
let y = 6;
let z = x + y;
```

### Using const

```JS
const x = 5;
const y = 6;
const z = x + y;
```

### One Statement, Many Variables

You can declare many variables in one statement.

Start the statement with let and separate the variables by comma:

```JS
let person = "John Doe", carName = "Volvo", price = 200;
```

A declaration can span multiple lines:

```JS
let person = "John Doe",
carName = "Volvo",
price = 200;
```

## Variable assignment

After a variable is declared, you can assign a value to it. The value can be anything, such as numbers, strings, objects, or even functions.

The Assignment operator "=" is used to assign values to JavaScript variables.

# Scoping

The Scope is the `region` of the code where a certain `variable` can be `accessed`.

In JavaScript there are 3 types of scope:

- Global scope
- Function/Local scope
- Block scope

## Global Scope

If a variable is declared outside all functions and curly braces ({}), then it is said to be defined in the Global Scope.

Variables declared with the var always have Global Scope.

Variables declared with the var keyword can NOT have block scope:

All scripts and functions on a web page can access Global variable.

```JS
{
  var x = 2;
}
// x CAN be used here
```

### Automatically Global

If you assign a value to a variable that has not been declared, it will automatically become a GLOBAL variable.

This code example will declare a global variable carName, even if the value is assigned inside a function.

```JS
myFunction();

// code here can use carName

function myFunction() {
  carName = "Volvo";
}
```

## Function Scope

JavaScript has function scope: Each function creates a new scope.

Variables defined inside a function are not accessible (visible) from outside the function.

Variables declared with var, let and const are quite similar when declared inside a function.

## Block Scope

If a variable is decalred with const or let within a curly brace({}), then it is said to be defined in the Block Scope

- if..else
- function(){}
- switch
- loops, etc.

Before ES6 (2015), JavaScript did not have Block Scope.

JavaScript had Global Scope and Function Scope.

ES6 introduced the two new JavaScript keywords: let and const.

These two keywords provided Block Scope in JavaScript:

Variables declared inside a { } block cannot be accessed from outside the block:

```JS
{
  let x = 2;
}
// x can NOT be used here
```

When a variable declared with let or const is accessed, Javascript searched for the variable in the block scopes first followed by global scopes.

### The Lifetime of JavaScript Variables

The lifetime of a JavaScript variable starts when it is declared.

Function (local) variables are deleted when the function is completed.

In a web browser, global variables are deleted when you close the browser window (or tab).
