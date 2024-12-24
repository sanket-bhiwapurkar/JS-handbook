# Hoisting

Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).

## JavaScript Declarations are Hoisted

In JavaScript, a variable can be declared after it has been used.

In other words; a variable can be used before it has been declared.

Example 1 gives the same result as Example 2:

Example 1

```JS
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element

var x; // Declare x
```

Example 2

```JS
var x; // Declare x
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;
```

This is due to Hoisting.

## The let and const Keywords

Variables defined with let and const are hoisted to the top of the block, but not initialized.

Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared.

Using a let variable before it is declared will result in a ReferenceError.

The variable is in a "temporal dead zone" from the start of the block until it is declared:

```JS
carName = "Volvo";
let carName;
//ReferenceError
```

Using a const variable before it is declared, is a syntax error, so the code will simply not run.

```JS
carName = "Volvo";
const carName;
```

## JavaScript Initializations are Not Hoisted

JavaScript only hoists declarations, not initializations.

Example 1 does not give the same result as Example 2:

Example 1

```JS
 var x = 5; // Initialize x
var y = 7; // Initialize y

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // 5 7
```

Example 2

```JS
 var x = 5; // Initialize x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // 5 undefined

var y = 7; // Initialize y
```

Does it make sense that y is undefined in the last example?

This is because only the declaration (var y), not the initialization (=7) is hoisted to the top.

Because of hoisting, y has been declared before it is used, but because initializations are not hoisted, the value of y is undefined.

Example 2 is the same as writing:

```JS
var x = 5; // Initialize x
var y;     // Declare y

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // Display x and y

y = 7;    // Assign 7 to y
```

# Redeclaring Variables

## Var Can be Redeclared

Redeclaring a JavaScript variable with var is allowed anywhere in a program:

```JS
 var x = 2;
// Now x is 2

var x = 3;
// Now x is 3
```

Redeclaring a variable using the var keyword can impose problems.

Redeclaring a variable inside a block will also redeclare the variable outside the block:

```JS
 var x = 10;
// Here x is 10

{
var x = 2;
// Here x is 2
}

// Here x is 2
```

## Let and Const Cannot be Redeclared

Variables defined with let and const can not be redeclared.

You can not accidentally redeclare a variable declared with let or const inside the same block.

```JS
let x = "John Doe";

let x = 0; //Error
```

```JS
var x = 2;     // Allowed
const x = 2;   // Not allowed

{
let x = 2;     // Allowed
const x = 2;   // Not allowed
}

{
const x = 2;   // Allowed
const x = 2;   // Not allowed
}
```

Redeclaring a variable inside a block will not redeclare the variable outside the block:

```JS
 let x = 10;
// Here x is 10

{
let x = 2;
// Here x is 2
}

// Here x is 10
```

```JS
 const x = 10;
// Here x is 10

{
const x = 2;
// Here x is 2
}

// Here x is 10
```

## Difference Between var, let and const

|       | Scope | Redeclare | Reassign | Hoisted | Binds this |
| ----- | ----- | --------- | -------- | ------- | ---------- |
| var   | No    | Yes       | Yes      | Yes     | Yes        |
| let   | Yes   | No        | Yes      | No      | No         |
| const | Yes   | No        | No       | No      | No         |

## What is Good?

let and const have block scope.

let and const can not be redeclared.

let and const must be declared before use.

let and const does not bind to this.

let and const are not hoisted.

## What is Not Good?

var does not have to be declared.

var is hoisted.

var binds to this.
